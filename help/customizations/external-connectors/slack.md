---
title: Slack外部连接器
description: 了解如何使用您自己的Slack应用程序在CX Enterprise Coworker中设置Slack外部连接器，并登录以在聊天中使用Slack对话。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="此连接器处于测试阶段。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 877954880bf6fda5151dcb343af92888db21cef4
workflow-type: tm+mt
source-wordcount: '2268'
ht-degree: 0%
---

# Slack外部连接器 {#slack}

使用[!DNL Slack]外部连接器在Adobe CX Enterprise Coworker中处理[!DNL Slack]对话。 设置连接器后，请要求同事搜索邮件和文件、读取渠道和线程以及查找人员。 如果管理员启用这些工具，您还可以发送邮件和回复。 连接器使用由[!DNL Slack]托管的正式远程模型上下文协议(MCP)服务器。

>[!AVAILABILITY]
>
>[!DNL Slack]外部连接器为Beta版。 文档和功能可能会发生变化。

## 连接器配置 {#connector-configuration}

连接器配置过程分为三个部分：

* **[!DNL Slack]应用程序准备：** [!DNL Slack]应用程序的所有者准备符合条件的应用程序，注册同事重定向URL，并设置用户范围。 Adobe不提供托管的[!DNL Slack]应用。
* **组织设置：**&#x200B;同事管理员为整个组织配置连接器一次。 管理员输入应用程序凭据并选择用户OAuth范围和成员可以使用的工具。
* **成员登录：**&#x200B;每个成员使用自己的[!DNL Slack]帐户登录。 成员只能访问其[!DNL Slack]帐户可以访问的内容。

连接器不使用共享机器人或共享[!DNL Slack]标识。 同事以登录成员身份发送邮件和回复。 保存组织配置不会登录任何成员或授予其他[!DNL Slack]访问权限。 每个成员必须单独登录。

## 先决条件 {#prerequisites}

在开始之前，请确保您具备以下条件：

* **同事访问：**&#x200B;在有[!DNL Slack]连接器的组织中，具有管理组织连接器的权限的帐户。
* **应用[!DNL Slack]：**&#x200B;已为您的工作区批准的内部应用或[!DNL Slack Marketplace]应用。 您还需要应用程序所有者，该所有者可以确认批准的用户范围并编辑应用程序设置。
* **应用程序凭据：**&#x200B;应用程序的客户端ID和客户端密钥，通过您用于处理凭据的批准流程共享。
* **工具和范围决策：**&#x200B;您的组织计划启用的读取、消息传递和草稿工具，以及计划请求的用户OAuth范围。
* **测试工作区或渠道：**&#x200B;检查与同意测试该工作区或渠道的成员之间的连接的地方。 请勿在客户或生产渠道中发送测试消息。

>[!IMPORTANT]
>
>切勿在屏幕截图、聊天或支持票证中共享客户端密钥、访问令牌或其他凭据。 仅在设置对话框的安全字段中输入凭据。

## 准备Slack应用程序 {#prepare-slack-app}

在Co-worker中配置连接器之前，应用程序所有者将准备[!DNL Slack]应用程序。 工作区或组织应用程序管理员可能还需要批准它。 有关[!DNL Slack]要求，请参阅[!DNL Slack]开发人员文档中的[Slack MCP服务器](https://docs.slack.dev/ai/slack-mcp-server/)。

### 选择符合条件的应用程序 {#choose-eligible-app}

[!DNL Slack]仅支持在[!DNL Slack Marketplace]中发布的内部自定义应用程序和应用程序的MCP服务器。 分发到组织外部的未列出应用不能使用[!DNL Slack] MCP服务器。 仅启用公共分发不会使应用程序符合条件。

1. 选择将拥有应用程序的工作区或组织，以及应用程序所有者。
1. 在[Slack应用程序管理](https://api.slack.com/apps)中，在该工作区中创建新应用程序。 要重用现有的符合条件的应用程序，请先获得其所有者的批准。
1. 在应用程序设置中，选择&#x200B;**[!UICONTROL 基本信息]** > **[!UICONTROL 应用程序凭据]**。 记下&#x200B;**[!UICONTROL 客户端ID]**&#x200B;和&#x200B;**[!UICONTROL 客户端密钥]**。

   在Co-worker中只输入这两个值。 请勿使用应用程序ID、签名密钥、机器人令牌或应用程序级令牌。

### 注册重定向URL {#register-redirect-url}

在[!DNL Slack]应用程序中注册同事重定向URL：

1. 在Co-worker中，打开&#x200B;**[!UICONTROL 连接Slack]**&#x200B;对话框，如[为组织配置连接器](#configure-organization)中所述。 复制&#x200B;**[!UICONTROL 重定向URL]**&#x200B;的完整值。

   您可以打开对话框以在完成或保存配置之前复制URL。

1. 在[!DNL Slack]应用程序设置中，选择&#x200B;**[!UICONTROL OAuth和权限]**。 在&#x200B;**[!UICONTROL 重定向URL]**&#x200B;下，添加完整的重定向URL，然后保存。

始终从所设置环境中的Co-worker对话框中复制重定向URL。 注册确切的方案、主机名、端口（如果存在）和路径。 请勿自己构建URL，或重用来自其他环境的重定向URL。 如果您使用多个环境，请单独注册每个重定向URL。

### 设置用户范围 {#set-user-scopes}

连接器使用用户OAuth范围，该范围授权每个成员的帐户。 它不使用机器人范围。

1. 在[!DNL Slack]应用程序设置中，选择&#x200B;**[!UICONTROL OAuth和权限]** > **[!UICONTROL 范围]** > **[!UICONTROL 用户令牌范围]**。
1. 添加您的组织批准的用户范围。 将它们与Co-worker中的[默认作用域](#review-scopes)进行比较，并仅添加您计划请求的作用域。

   默认作用域是Co-worker的默认功能集，而不是[!DNL Slack]要求的最低值。 使用粒度`search:read.*`范围，而不是较旧的`search:read`范围。 在应用程序清单中，用户作用域属于`oauth_config.scopes.user`，而非`oauth_config.scopes.bot`。

`chat:write`用户范围允许同事以登录成员身份发送消息。 如果您的组织不计划发送消息，请将其忽略。

您的工作区或[!DNL Slack]企业组织可能需要应用程序批准和范围审查。 应用程序批准不会取代每个成员的同意。 仅允许[!DNL Slack Marketplace]个应用的策略可以阻止内部应用。 有关详细信息，请参阅[管理您工作区的应用审批](https://slack.com/help/articles/222386767-Manage-app-approval-for-your-workspace)。

如果您的应用程序使用允许的IP地址限制，[!DNL Slack]也会将这些限制应用于MCP请求。 请联系您的Adobe代表以确认允许的地址。 不要猜测IP地址范围。 某些功能（如语义搜索）可能取决于您的[!DNL Slack]计划。

### 查看不可逆应用程序设置 {#review-irreversible-settings}

同事使用客户端ID和客户端密钥作为机密的OAuth客户端进行连接。 某些[!DNL Slack]应用程序设置无法撤消，因此在更改它们之前请查看以下设置：

* **用于代码交换(PKCE)的验证密钥：**&#x200B;未经确认请勿打开此连接器的[!DNL Slack] PKCE设置。 [!DNL Slack]个文档（此设置将应用程序更改为公共客户端），只有[!DNL Slack]支持人员才能将其还原。 有关详细信息，请参阅[使用PKCE](https://docs.slack.dev/authentication/using-pkce/)。
* **令牌轮换：** [!DNL Slack]令牌轮换在打开后无法关闭。 在为此应用程序启用此功能之前，请联系您的Adobe代表。 有关详细信息，请参阅[使用令牌轮换](https://docs.slack.dev/authentication/using-token-rotation/)。

### 不需要机器人功能 {#bot-features-not-required}

连接器不需要机器人功能。 您不需要机器人令牌范围、[!DNL Events API]请求URL、交互性请求URL、传入webhook、斜杠命令、[!DNL Socket Mode]或应用程序级别的令牌。 如果现有应用程序将这些功能用于其他目的，请保留它们。

[!DNL Slack] MCP服务器不支持动态客户端注册或服务器发送的事件(SSE)。 Co-worker使用您的注册应用程序和可流式处理HTTP传输。

## 为您的组织配置连接器 {#configure-organization}

管理员使[!DNL Slack]连接器对组织中的每个人可用。 组织页面上的更改适用于组织中的所有用户。 在成员登录之前完成[准备Slack应用程序](#prepare-slack-app)。

1. 打开&#x200B;**[!UICONTROL 自定义项]**，选择&#x200B;**[!UICONTROL 组织]**，然后选择&#x200B;**[!UICONTROL 外部连接器]**。 在&#x200B;**[!UICONTROL Slack]**&#x200B;信息卡上，选择&#x200B;**[!UICONTROL 配置]**。

   将打开&#x200B;**[!UICONTROL 连接Slack]**&#x200B;对话框。 连接器使用固定的[!DNL Slack] MCP服务器URL `https://mcp.slack.com/mcp`。 使用此配置的组织范围，而不是个人连接。

1. 确保已在您的应用程序中注册&#x200B;**[!UICONTROL Slack应用程序]**&#x200B;下的&#x200B;**[!UICONTROL 重定向URL]**，如[注册重定向URL](#register-redirect-url)中所述。 然后输入您应用程序的&#x200B;**[!UICONTROL 客户端ID]**&#x200B;和&#x200B;**[!UICONTROL 客户端密钥]**。 这两个字段都是必填字段。

   请勿输入应用程序ID、签名密钥或机器人令牌。 同事将凭据作为机密存储，而不是作为纯文本连接器设置存储。

   ![连接Slack对话框，其中显示了Slack应用程序部分，该部分带有密文的重定向URL、空的客户端ID和客户端密钥字段、默认的用户OAuth作用域以及用户可用的第一个工具。](./assets/slack/org-configure.png){width="500" zoomable="yes"}

1. 查看&#x200B;**[!UICONTROL 用户OAuth范围]**。 有关详细信息，请参阅[查看用户OAuth作用域](#review-scopes)。

1. 在&#x200B;**[!UICONTROL 用户可用的工具]**&#x200B;下，删除成员不应使用的任何工具。 必须至少保留一个工具。 有关详细信息，请参阅[可用工具](#available-tools)。

1. 查看&#x200B;**[!UICONTROL 访问和权限]**，然后选择&#x200B;**[!UICONTROL 保存连接]**。 **[!UICONTROL Slack]**&#x200B;卡片显示&#x200B;**[!UICONTROL 已保存的配置]**。

   该对话框还显示&#x200B;**[!UICONTROL 身份验证]**&#x200B;方法、**[!UICONTROL 连接]**&#x200B;类型和&#x200B;**[!UICONTROL 工具超时]**。 当凭据字段或范围列表为空时，Co-worker不会保存配置。

   重新加载页面，选择&#x200B;**[!UICONTROL 查看配置]**，并确认配置和工具选择已在成员登录之前保存。

   ![连接Slack对话框，其中显示用户OAuth范围、用户可用的所有16个工具、访问和权限通知、OAuth身份验证、HTTP连接以及60秒工具超时设置。](./assets/slack/org-scopes-tools.png){width="500" zoomable="yes"}

保存操作不会将您或任何成员登录到[!DNL Slack]。 要检查连接，请按照[以成员身份登录](#sign-in-as-a-member)中的说明以自己的身份登录。

### 查看用户OAuth范围 {#review-scopes}

**[!UICONTROL 用户OAuth范围]**&#x200B;字段为必填。 用空格或逗号分隔范围，并与为您的应用程序批准的用户范围匹配。 默认情况下，该字段包含以下22个范围：

```text
search:read.public search:read.private search:read.im search:read.mpim search:read.files search:read.users channels:history groups:history im:history mpim:history channels:read groups:read im:read mpim:read users:read users:read.email files:read canvases:read lists:read emoji:read reactions:read chat:write
```

您的工作区可能不会批准每个默认范围。 与应用程序所有者一起查看请求的范围。

>[!IMPORTANT]
>
>默认范围包括专用内容，如专用渠道、组消息和私信。 它们还包括`chat:write`，允许同事以登录成员身份发送邮件和回复。 明确确定贵组织是否启用消息发送工具。 删除工具不会删除其OAuth作用域。 如果不希望成员发送消息，请删除`slack_send_message`工具和`chat:write`范围。

工具选择和OAuth范围是相互独立的。 缩小访问范围时，请同时查看工具列表和范围字段。 启用的工具不向成员授予超出其帐户权限的[!DNL Slack]访问权限。

### 可用工具 {#available-tools}

[!DNL Slack]连接器提供以下16个工具。 默认情况下，成员可以使用所有这些功能。

| 功能 | 工具 |
| --- | --- |
| 搜索 | `slack_search_public` |
| 搜索 | `slack_search_public_and_private` |
| 搜索 | `slack_search_channels` |
| 搜索 | `slack_search_users` |
| 读取对话 | `slack_read_channel` |
| 读取对话 | `slack_read_thread` |
| 读取对话 | `slack_list_channel_members` |
| 读取对话 | `slack_list_user_channels` |
| 读取内容和配置文件 | `slack_read_canvas` |
| 读取内容和配置文件 | `slack_read_user_profile` |
| 读取内容和配置文件 | `slack_read_file` |
| 读取内容和配置文件 | `slack_read_list` |
| 表情符号和反应 | `slack_search_emojis` |
| 表情符号和反应 | `slack_get_reactions` |
| 消息和草稿 | `slack_send_message` |
| 消息和草稿 | `slack_send_message_draft` |

连接器不是只读的。 除非您删除`slack_send_message`工具，否则成员可以发送邮件和回复。 不包括渠道创建、计划消息、文件上传、添加反应以及画布或列表更改。

## 以成员身份登录 {#sign-in-as-a-member}

管理员配置连接器后，每个成员均使用自己的[!DNL Slack]帐户登录。 您不需要客户端密码即可登录。

1. 打开&#x200B;**[!UICONTROL 自定义项]**，选择&#x200B;**[!UICONTROL 用户]**，然后选择&#x200B;**[!UICONTROL 外部连接器]**。

1. 查找&#x200B;**[!UICONTROL Slack]**&#x200B;卡。 如果卡片显示&#x200B;**[!UICONTROL 未配置]**&#x200B;和&#x200B;**[!UICONTROL 尚不可用。 您的管理员需要设置此项。]**，请要求您的管理员[配置连接器](#configure-organization)。

   请勿索取或复制组织的客户端密钥。

1. 管理员配置连接器后，**[!UICONTROL Slack]**&#x200B;卡显示&#x200B;**[!UICONTROL 需要登录]**。 Select **[!UICONTROL 在信息卡上登录]**。

   您还可以打开&#x200B;**[!UICONTROL Slack]**&#x200B;连接器详细信息。 登录之前，**[!UICONTROL 连接]**&#x200B;部分显示&#x200B;**[!UICONTROL 未登录]**，使用&#x200B;**[!UICONTROL 登录]**&#x200B;按钮。

   ![成员的Slack连接器详细信息，显示需要登录的状态、“测试连接”按钮、服务器URL、每个用户登录、未使用登录按钮登录以及管理员启用的工具。](./assets/slack/member-details.png){width="700" zoomable="yes"}

1. 使用您计划使用的[!DNL Slack]帐户和工作区完成[!DNL Slack]授权。 查看请求的权限和任何工作区审批要求。

   >[!IMPORTANT]
   >
   >只有在您识别应用程序并且组织批准请求的访问权限时，才应继续。

1. 返回到同事并检查连接状态。 Select **[!UICONTROL 测试连接]**，然后[检查您的Slack访问权限](#check-access)，然后再依赖该连接。

1. 仔细查看消息传送操作。 同事将邮件和回复作为您的[!DNL Slack]帐户发送。

作为成员，您可以测试连接或注销，但无法更改组织设置。 您只能访问[!DNL Slack]和授予的作用域允许的内容。 此内容仅在您自己的[!DNL Slack]帐户可以访问私人对话时才包含私人对话。

若要从连接器断开您的[!DNL Slack]帐户，请选择&#x200B;**[!UICONTROL 注销]**。

## 检查您的Slack访问权限 {#check-access}

要确认连接器可以读取您的[!DNL Slack]内容，请开始聊天并输入只读提示。 确保您的管理员启用了`slack_list_user_channels`工具。

示例提示：

* “使用Slack，列出最多五个我所属的渠道。 仅显示渠道名称。 请勿发送消息、创建草稿或更改任何内容。”

如果贵组织启用消息传送工具，请仅在专供测试并获批准的渠道中测试发送。 要求第二个成员单独登录，并确认每个成员只能看到自己的[!DNL Slack]内容。

## 访问疑难解答 {#troubleshoot-access}

如果设置、登录或访问失败，请与管理员核对以下事项：

| 问题 | 检查内容 |
| --- | --- |
| 无法保存设置 | 输入客户端ID和客户端密钥，至少保留一个用户OAuth范围，并至少保留一个工具。 请勿输入应用程序ID、签名密钥或机器人令牌。 |
| **[!UICONTROL 重定向URL]**&#x200B;缺失，或[!DNL Slack]报告重定向不匹配 | 比较辅助进程对话框中的完整重定向URL（包括方案、主机、端口和路径）与保存在[!DNL Slack]应用程序中的&#x200B;**[!UICONTROL 重定向URL]**。 如果URL缺失或值不同，请联系您的Adobe代表。 |
| [!DNL Slack]登录或请求失败 | 检查应用审批、授予的用户范围、[!DNL Slack]帐户和工作区以及应用上的任何IP地址限制。 如果请求一直失败，请注销，然后重新登录。 |
| 读取或发送操作不可用 | 检查组织的工具选择、请求的和已授予的作用域，以及成员的[!DNL Slack]权限。 这些设置是独立的。 |
| 成员无法更改应用程序设置 | 对于组织管理的连接，会发生此行为。 询问管理员。 成员绝不输入组织的客户端密码。 |
