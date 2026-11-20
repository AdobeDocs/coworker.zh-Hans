---
title: RainFocus外部连接器
description: 了解如何在CX Enterprise Coworker中为您的组织设置RainFocus外部连接器，并使用RainFocus登录以在聊天中使用事件数据工具。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="此连接器处于测试阶段。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: e65f811f1e9c27de372ce924301b68f20ab9c1a6
workflow-type: tm+mt
source-wordcount: '2116'
ht-degree: 0%
---

# RainFocus外部连接器 {#rainfocus}

使用[!DNL RainFocus]外部连接器在Adobe CX Enterprise Coworker中使用[!DNL RainFocus]事件数据。 设置连接器后，请向同事询问您的[!DNL RainFocus]帐户可以访问的会话、出席者和自定义属性。 连接器使用[!DNL RainFocus] MCP配置文件，它是由[!DNL RainFocus]托管的模型上下文协议(MCP)服务器。

>[!AVAILABILITY]
>
>[!DNL RainFocus]外部连接器为Beta版。 文档和功能可能会发生变化。

## 连接器配置 {#connector-configuration}

连接器配置过程分为三个部分：

* **[!DNL RainFocus]准备：** [!DNL RainFocus]管理员设置MCP配置文件，启用其工具，并提供配置文件URL。 每个成员都需要具有正确角色的[!DNL RainFocus]帐户。
* **组织设置：**&#x200B;同事管理员为整个组织保存一次MCP配置文件URL。 连接器启用读取工具的固定列表。
* **成员登录：**&#x200B;每个成员使用自己的[!DNL RainFocus]帐户登录。 成员只能访问其[!DNL RainFocus]角色和配置文件允许的数据。

保存组织配置不会登录任何成员、授予[!DNL RainFocus]权限或运行[!DNL RainFocus]数据工具。 每个成员必须单独登录。

## 先决条件 {#prerequisites}

在开始之前，请确保您具备以下条件：

* **同事访问：**&#x200B;在有[!DNL RainFocus]连接器的组织中，已打开组织设置的同事管理员帐户。
* **MCP配置文件：**&#x200B;已设置的[!DNL RainFocus] MCP配置文件及其完整的HTTPS配置文件URL，由您的[!DNL RainFocus]管理员提供。 有关详细信息，请参阅[获取MCP配置文件URL](#get-profile-url)。
* **成员帐户：**&#x200B;对于每个成员，都有一个[!DNL RainFocus]帐户，该帐户具有允许访问所需数据的安全角色。

您未在协同工作中输入客户端ID、客户端密钥或访问令牌。 每个成员都使用自己的帐户登录[!DNL RainFocus]。

## 准备[!DNL RainFocus]访问权限 {#prepare-rainfocus}

在Co-worker中配置连接器之前，请在[!DNL RainFocus]中准备MCP配置文件和成员访问权限。 [!DNL RainFocus]拥有配置文件、其启用的工具、成员角色和任何费用。 Co-worker存储您组织的配置文件URL和工具列表，以及每个成员的登录。

### 获取MCP配置文件URL {#get-profile-url}

[!DNL RainFocus]通常会根据客户的要求为其配置MCP配置文件。 如果[!DNL RainFocus]管理员设置了配置文件，则流程如下所示：

1. 在[!DNL RainFocus]中，打开&#x200B;**[!UICONTROL 集成套件]** > **[!UICONTROL 活动配置文件]** > **[!UICONTROL MCP配置文件]**，然后创建配置文件。
1. 仅启用用例所需的工具，并关闭其他工具。
1. 复制生成的MCP服务器URL。 URL特定于配置文件。

将完整URL提供给配置连接器的同事管理员。 请勿猜测配置文件名称或自行构建URL。 有关详细信息，请参阅[RainFocus MCP配置文件公告](https://www.rainfocus.com/company/news-press/rainfocus-launches-ai-agent-connectivity-for-event-data-with-mcp-profiles/)。

### 确认成员访问权限 {#confirm-member-access}

每个成员均使用自己的[!DNL RainFocus]帐户登录。 帐户的安全角色以及在配置文件中启用的工具控制成员可以访问哪些数据。 请咨询[!DNL RainFocus]管理员，确认每个成员的任务权限最低。

## 为您的组织配置连接器 {#configure-organization}

管理员使[!DNL RainFocus]连接器对组织中的每个人可用。 组织页面上的更改适用于组织中的所有用户。 **[!UICONTROL 组织]**&#x200B;范围仅对打开了组织设置的管理员显示。

1. 打开&#x200B;**[!UICONTROL 自定义项]**，选择&#x200B;**[!UICONTROL 组织]**，然后选择&#x200B;**[!UICONTROL 外部连接器]**。
1. 查找具有Beta标签并显示&#x200B;**[!UICONTROL 未配置]**&#x200B;的&#x200B;**[!UICONTROL RainFocus]**&#x200B;卡。 选择&#x200B;**[!UICONTROL 配置]**。

1. 在&#x200B;**[!UICONTROL 设置RainFocus]**&#x200B;对话框中，输入&#x200B;**[!UICONTROL 开发配置文件URL]**。 使用[!DNL RainFocus]管理员提供的完整MCP配置文件URL。

   URL必须以`https://`开头。 它不能包含空格、反斜杠、查询字符串(`?`)、片段(`#`)、用户名或密码、非默认端口或`.`或`..`路径段。 如果URL与规则不匹配，Co-worker将显示一条说明该规则的消息。 Co-worker仅检查URL的格式。 它不会检查配置文件是否存在或您能否使用它。

1. 查看&#x200B;**[!UICONTROL 访问和权限]**&#x200B;和&#x200B;**[!UICONTROL 固定读取工具]**&#x200B;部分。 连接器启用所有10个读取工具，您无法在此对话框中添加、删除或编辑它们。 某些工具会返回与会者个人数据或批量导出。 有关详细信息，请参阅[可用工具](#available-tools)。

   ![设置RainFocus对话框，其中显示空的开发配置文件URL字段、“访问和权限”部分、“固定读取工具”（包含10个工具）以及“保存连接”按钮。](./assets/rainfocus/org-configure.png){width="500" zoomable="yes"}

1. Select **[!UICONTROL 保存连接]**。 当同事保存连接时，您无法编辑或取消表单。

如果保存失败，对话框将显示&#x200B;**[!UICONTROL 无法保存连接]**&#x200B;并保留您输入的URL。 即使保存失败，也可能会保存某些设置。 重新打开配置并检查它，然后重试。 要避免发生冲突的更改，请确保一次只能由一位管理员配置连接器。

### 验证保存的配置 {#verify-configuration}

保存连接后，检查配置：

1. 保存后，该对话框将打开保存的连接器详细信息。 返回&#x200B;**[!UICONTROL 外部连接器]**&#x200B;列表，并确认&#x200B;**[!UICONTROL RainFocus]**&#x200B;卡显示已保存的&#x200B;**[!UICONTROL 配置]**&#x200B;和&#x200B;**[!UICONTROL 查看配置]**。
1. 重新加载页面，然后选择&#x200B;**[!UICONTROL 查看配置]**。
1. 确认以下详细信息：

   * **[!UICONTROL Source]**&#x200B;显示您输入的配置文件URL。
   * **[!UICONTROL 身份验证]**&#x200B;存在。
   * **[!UICONTROL 工具策略]** > **[!UICONTROL 允许的工具名称或模式]**&#x200B;列出与[可用工具](#available-tools)部分相同的10个工具。

1. 要检查您自己的连接，请选择&#x200B;**[!UICONTROL 测试]**。 如果同事要求您登录，请使用您自己的[!DNL RainFocus]帐户，如[以成员身份登录](#sign-in-as-a-member)中所述。

   **[!UICONTROL Test]**&#x200B;列出了服务器的工具并更新了&#x200B;**[!UICONTROL 工具]**&#x200B;计数。 如果服务器未返回任何工具，则详细信息显示&#x200B;**[!UICONTROL 0个可用的工具]**。 如果测试失败，详细信息将显示&#x200B;**[!UICONTROL 连接失败]**。

   ![保存的Rainfocus连接器详细信息显示密文的源、Rainfocus_login身份验证方法、未登录的登录按钮以及“测试和删除”按钮。](./assets/rainfocus/org-details.png){width="700" zoomable="yes"}

连接器详细信息上的&#x200B;**[!UICONTROL 连接]**、**[!UICONTROL 测试]**&#x200B;和登录控件仅适用于您自己的连接。 当您以管理员身份登录时，没有成员登录。 成功的测试仅列出工具。 测试未运行[!DNL RainFocus]数据工具或确认成员可以访问特定数据。

连接器详细信息没有用于编辑配置文件URL的选项。 **[!UICONTROL 移除]**&#x200B;打开确认，然后移除整个组织的连接。 将删除视为管理员的慎重决定，而不是故障排除步骤。

### 可用工具 {#available-tools}

[!DNL RainFocus]连接器启用10个读取工具的固定列表：

| 工具 | 数据区域 |
| --- | --- |
| `get_attendeeInfo` | 与会者 |
| `get_attendee_load` | 与会者 |
| `get_attendee_search` | 与会者 |
| `get_attribute_load` | 自定义属性 |
| `get_attribute_search` | 自定义属性 |
| `get_attributevalue_load` | 自定义属性 |
| `get_entityDataDump_attendee` | 与会者，批量导出 |
| `get_entityDataDump_session` | 会话，批量导出 |
| `get_session_load` | Sessions |
| `get_session_search` | Sessions |

此列表中不存在的工具（包括[!DNL RainFocus]以后添加的工具）不会自动启用。 该列表未替换[!DNL RainFocus]安全角色或配置文件的工具设置，这些设置仍控制对数据的访问。

>[!IMPORTANT]
>
>多个工具可以返回与与会者有关的个人数据和联系信息。 两种工具可批量导出数据，其结果可能会非常大。 根据您的[!DNL RainFocus]条款，阅读工作也可能产生费用。 在成员登录之前，请与数据治理所有者一起查看这些工具。

## 以成员身份登录 {#sign-in-as-a-member}

管理员配置连接器后，每个成员均使用自己的[!DNL RainFocus]帐户登录。 您不需要客户端ID、客户端密钥或访问令牌即可登录。

1. 打开&#x200B;**[!UICONTROL 自定义项]**，然后选择&#x200B;**[!UICONTROL 外部连接器]**。 成员默认使用&#x200B;**[!UICONTROL 用户]**&#x200B;范围。 查找&#x200B;**[!UICONTROL RainFocus]**&#x200B;卡。
1. 如果该卡显示&#x200B;**[!UICONTROL 尚不可用。 您的管理员需要设置此项。]**，请要求您的管理员[配置连接器](#configure-organization)。 成员无法输入自己的配置文件URL。
1. 检查卡上的状态。 卡片显示&#x200B;**[!UICONTROL 需要登录]**、**[!UICONTROL 已连接]**、**[!UICONTROL 由管理员设置]**&#x200B;或&#x200B;**[!UICONTROL 连接失败]**&#x200B;状态。

   **[!UICONTROL 由您的管理员设置]**&#x200B;意味着同事无法确认您的登录状态。 这并不意味着您已登录或注销。

1. Select **[!UICONTROL 登录]**。 您还可以打开卡片详细信息并选择&#x200B;**[!UICONTROL 连接]**&#x200B;部分中的&#x200B;**[!UICONTROL 登录]**。 在[!DNL RainFocus]窗口中，完成登录、单点登录(SSO)、多重身份验证(MFA)和同意提示。 查看您批准的访问权限。

   如果出现&#x200B;**[!UICONTROL 发现授权]**，则同事将读取服务器的登录详细信息，而不是其工具。 如果发现失败，或面板要求&#x200B;**[!UICONTROL 客户端ID]**&#x200B;或&#x200B;**[!UICONTROL 客户端密钥]**，请停止并与管理员联系。 请勿输入或猜测凭据。

   ![成员的RainFocus连接器详细信息，显示需要登录的状态、密文的服务器URL、每个用户登录、未使用“发现授权”按钮登录以及管理员启用的10个工具。](./assets/rainfocus/member-details.png){width="700" zoomable="yes"}

1. 返回到Co-worker并确认状态是否显示&#x200B;**[!UICONTROL 已连接]**。 仅关闭的登录窗口无法确认成功。 如果提前关闭窗口，则不会发生任何更改，可以重试。
1. 打开卡片详细信息以从管理员处查看设置。 您可以查看管理员启用的&#x200B;**[!UICONTROL 服务器URL]**、**[!UICONTROL 登录者]**、**[!UICONTROL 身份验证]**&#x200B;和&#x200B;**[!UICONTROL 工具]**。
1. Select **[!UICONTROL 在信息卡上测试]**，或在详细信息中测试&#x200B;**[!UICONTROL 连接]**，以检查与帐户的连接。

   成功的测试显示[!DNL RainFocus]使用您的帐户响应了可用的工具数量。 测试仅列出工具。 它不会运行数据工具或确认对特定事件或记录的访问权限。 若要续订您的登录并再次列出工具，请选择&#x200B;**[!UICONTROL 刷新]**。 如果同事无法续订您的登录，则按钮会显示&#x200B;**[!UICONTROL 重新加载工具]**，它只再次列出这些工具。

1. 如果测试失败，同事显示&#x200B;**[!UICONTROL 无法连接到RainFocus]**，请重试&#x200B;]**并**[!UICONTROL &#x200B;技术详细信息&#x200B;]**。**[!UICONTROL &#x200B;如果您已注销，请重新登录。 如果问题仍然存在，请与管理员联系。

成员可以登录、注销、测试、刷新和查看启用的工具。 成员无法更改或删除组织连接、编辑配置文件URL或更改工具。 打开详细信息的每个成员都可以查看配置文件URL。 管理员登录时，其他成员未登录。

若要从连接器断开您的[!DNL RainFocus]帐户，请选择&#x200B;**[!UICONTROL 注销]**。 您可以随时重新登录。

## 检查您的事件数据访问权限 {#check-event-access}

要确认您可以使用[!DNL RainFocus]数据，请运行具有窄请求的只读检查。 使用您获准处理的事件，并避免使用返回与会者数据或批量导出的工具来执行此检查。 开始聊天并输入提示。

示例提示：

* “使用RainFocus，最多可以找到五个我可以访问的会议。 如果返回了会话标题和ID，则仅显示它们。 请勿导出数据、返回与会者信息或更改任何内容。”

确认结果中包含您期望的会话。 空结果并不总是意味着连接器无法正常工作。 检查用于登录的[!DNL RainFocus]帐户、安全角色以及配置文件中启用的工具。 如果结果异常大或包含敏感数据，请停止并缩小请求。

## 访问疑难解答 {#troubleshoot-access}

如果您无法访问您的[!DNL RainFocus]数据，请与管理员核对以下事项：

| 问题 | 检查内容 |
| --- | --- |
| 缺少&#x200B;**[!UICONTROL RainFocus]**&#x200B;卡 | 与您的Adobe代表确认您的组织可以使用连接器。 |
| **[!UICONTROL 组织]**&#x200B;范围缺失 | 确认您是管理员，并且已为您的组织打开组织设置。 |
| 同事拒绝了配置文件URL | 遵循消息中的规则。 使用[!DNL RainFocus]管理员提供的完整配置文件URL，并且不要猜测配置文件名称。 |
| **[!UICONTROL 无法保存连接]**&#x200B;出现 | 可能会保存某些设置。 重新打开配置并检查它，然后重试。 确保一次只能有一个管理员配置连接器。 |
| 卡片显示&#x200B;**[!UICONTROL 尚不可用。 您的管理员需要设置此项。]** | 缺少组织设置。 要求您的管理员[配置连接器](#configure-organization)。 |
| 登录要求&#x200B;**[!UICONTROL 客户端ID]**&#x200B;或&#x200B;**[!UICONTROL 客户端密钥]**，否则发现失败 | 停止并联系您的管理员。 请勿输入或猜测凭据或注册应用程序。 |
| 在[!DNL RainFocus]中审批访问后，登录失败 | 检查您使用的[!DNL RainFocus]帐户和安全角色。 请让您的Adobe代表和[!DNL RainFocus]检查您环境的登录设置。 不要共享登录URL。 |
| **[!UICONTROL 测试]**&#x200B;成功，但数据请求失败 | **[!UICONTROL 测试]**&#x200B;仅列出工具。 检查您的[!DNL RainFocus]安全角色、在配置文件中启用的工具以及工具所需的过滤器。 |
| 登录时&#x200B;**[!UICONTROL 无法连接到RainFocus]** | Select **[!UICONTROL 请重试]**。 如果问题仍然存在，请与管理员联系。 |
| 结果异常大或包含敏感数据 | 停止并缩小您的请求。 请勿将原始事件数据粘贴到票证或聊天中。 |

当您联系支持人员时，请仅包含错误文本、错误时间和您的环境。 请勿共享技术详细信息、个人资料URL、登录捕获、密码、令牌或授权码。
