---
title: Amazon Ads外部连接器
description: 了解如何在CX Enterprise Coworker中为您的组织设置Amazon Ads外部连接器，并使用Amazon登录以在聊天中使用Amazon Ads工具。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="此连接器处于测试阶段。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 80dda0b442d6c7fe560c965b985f58173b73fe13
workflow-type: tm+mt
source-wordcount: '3078'
ht-degree: 1%
---

# Amazon Ads外部连接器 {#amazon-ads}

使用[!DNL Amazon Ads]外部连接器在Adobe CX Enterprise Coworker中处理[!DNL Amazon Ads]数据。 设置连接器后，询问同事您可以访问哪些广告帐户，并查看营销活动、报告、账单和其他帐户信息。 连接器是由[!DNL Amazon]托管的模型上下文协议(MCP)服务器。

>[!AVAILABILITY]
>
>[!DNL Amazon Ads]外部连接器为Beta版。 文档和功能可能会发生变化。

## 连接器配置 {#connector-configuration}

连接器配置过程分为三个部分：

* **[!DNL Amazon]准备：** [!DNL Amazon Ads]帐户管理员为每个成员授予他们所需的广告帐户的访问权限。 如果您的组织使用其自己的OAuth应用程序，则应用程序所有者会确认其批准并注册同事重定向URL。
* **组织设置：**&#x200B;同事管理员为整个组织配置连接器一次。 管理员选择区域、OAuth应用程序以及成员可以使用的工具。
* **成员登录：**&#x200B;每个成员使用自己的[!DNL Amazon]帐户登录。 成员只能访问其[!DNL Amazon]帐户具有使用权限的广告帐户。

保存组织配置不会登录任何成员或授予[!DNL Amazon Ads]权限。 每个成员都必须在[!DNL Amazon Ads]中拥有所需的访问权限，并且必须单独登录。

## 先决条件 {#prerequisites}

在开始之前，请确保您具备以下条件：

* **同事访问：**&#x200B;在有[!DNL Amazon Ads]连接器的组织中，具有管理组织连接器的权限的帐户。
* **Advertising帐户：**&#x200B;您计划使用的广告帐户及其[!DNL Amazon Ads]区域，以及具有这些帐户所需权限的成员。 有关详细信息，请参阅[授予广告帐户访问权限](#grant-member-access)。
* **OAuth应用程序决策：**&#x200B;选择以下选项：
  * **Adobe管理的OAuth应用程序：** Adobe管理应用程序注册及其凭据。 托管应用程序必须在您的环境中可用。
  * **您自己的OAuth应用程序：**&#x200B;已为[!DNL Amazon Ads] API批准的[!DNL Login with Amazon]应用程序、其OAuth客户端ID和客户端密钥，以及可以编辑其安全配置文件的管理员。 已注册的安全性配置文件本身不授予[!DNL Amazon Ads] API批准。

引导式设置支持每个组织一个[!DNL Amazon Ads]连接和一个区域。 每个成员均使用自己的[!DNL Amazon]帐户登录。 Adobe管理的应用程序是共享应用程序注册，而不是共享[!DNL Amazon]帐户。

## 准备Amazon访问权限 {#prepare-amazon}

在Co-worker中配置连接器之前，请在[!DNL Amazon]中准备您的应用和帐户访问权限。 应用程序设置访问和广告数据访问是分开的。 使用连接器的成员无需权限即可编辑应用程序。

### 确认应用程序审批 {#confirm-app-approval}

如果您使用自己的OAuth应用程序，请要求应用程序所有者确认正确的[!DNL Login with Amazon]安全配置文件及其[!DNL Amazon Ads] API审批。 创建安全配置文件或在[!DNL Amazon]开发人员控制台中查看应用程序不会取代[!DNL Amazon Ads] API审批。 有关详细信息，请参阅[!DNL Amazon Ads]文档中的[Amazon Ads MCP快速入门](https://advertising.amazon.com/API/docs/en-us/mcp/get-started)和[使用OAuth连接到Ads MCP服务器](https://advertising.amazon.com/API/docs/en-us/mcp/oauth)。

对于您自己的应用程序，同事会自动应用以下设置。 请不要在“设置”对话框中输入这些值。

| 设置 | 值 |
| --- | --- |
| 授权 URL | `https://lwa.amazon.com/ap/oa` |
| 令牌 URL | `https://api.amazon.com/auth/o2/token` |
| 请求的范围 | `advertising::campaign_management` |
| 用于代码交换(PKCE)的Proof密钥 | 已启用 |
| 令牌端点客户端身份验证 | `client_secret_post`，作为机密客户端 |
| 动态客户端注册 | 不受支持 |
| 传输和工具超时 | 可流式处理HTTP，60秒 |

如果您使用Adobe管理的OAuth应用程序，则Adobe会管理应用程序注册及其凭据。 您无需完成此步骤或输入应用程序凭据。

### 注册重定向URL {#register-redirect-url}

如果您使用自己的OAuth应用程序，请在[!DNL Login with Amazon]应用程序中注册同事重定向URL：

1. 在同事中，打开&#x200B;**[!UICONTROL 为您的组织配置Amazon广告]**&#x200B;对话框，如[为您的组织配置连接器](#configure-organization)中所述。 Select **[!UICONTROL 使用我自己的OAuth应用程序]**&#x200B;显示&#x200B;**[!UICONTROL 重定向URL]**，然后复制完整的值。
1. 在[使用Amazon控制台登录](https://developer.amazon.com/loginwithamazon/console/site/lwa/overview.html)中，查找应用程序的安全配置文件。 Select **[!UICONTROL 管理]** > **[!UICONTROL Web设置]**，然后选择&#x200B;**[!UICONTROL 编辑]**。
1. 在&#x200B;**[!UICONTROL 允许的返回URL]**&#x200B;下添加完整的重定向URL，然后保存。 如果其他团队共享应用程序，请保留现有URL并在更改设置之前获得应用程序所有者的批准。
1. 记下来自同一安全配置文件的OAuth客户端ID和客户端密码。 在[配置连接器](#configure-organization)时输入它们。

始终从所设置环境中的Co-worker对话框中复制重定向URL。 请不要自己构建URL，请在浏览器中使用同事页面的URL，或者重复使用来自其他环境或MCP客户端的重定向URL。 有关详细信息，请参阅[!DNL Amazon]文档中的[注册Amazon登录](https://developer.amazon.com/docs/login-with-amazon/register-web.html)。

>[!NOTE]
>
>如果&#x200B;**[!UICONTROL 重定向URL]**&#x200B;只显示路径`/connectors/oauth/callback`，则您的环境尚不支持此连接器的登录。 请勿注册部分路径或猜测主机名。 联系您的 Adobe 代表。

### 授予广告帐户访问权限 {#grant-member-access}

[!DNL Amazon Ads]帐户管理员邀请每个成员访问他们需要的广告帐户：

1. 打开[Amazon广告控制台](https://advertising.amazon.com/)，然后选择&#x200B;**[!UICONTROL 更改帐户]**&#x200B;以选择广告商或经理帐户。
1. Select **[!UICONTROL 管理]** > **[!UICONTROL 帐户访问和设置]** > **[!UICONTROL 用户]** > **[!UICONTROL 邀请用户]**。 确切的选项取决于帐户类型。 邀请成员的[!DNL Amazon]帐户，并具有计划执行任务的最低权限。
1. 对于经理帐户，检查访问权限是涵盖整个经理帐户，还是仅涵盖选定的链接广告商。 要求成员接受与同事使用相同[!DNL Amazon]帐户的邀请。
1. 确认成员可以在[!DNL Amazon Ads]中选择广告商。 请记下已批准内部记录中预期的帐户名称、地区和广告商ID，以便您稍后在同事中确认访问权限。

选择支持您计划任务的最低权限角色。 不要仅授予管理员访问权限以使访问检查成功。 访问[!DNL Amazon Marketing Cloud]实例与访问广告商营销活动是分开的。 有关详细信息，请参阅以下[!DNL Amazon Ads]文档：

* [以Manager帐户管理用户](https://advertising.amazon.com/help/G4M4JGKGV2VAY9JC)
* [在您的帐户中添加或删除用户](https://advertising.amazon.com/help/GDQVHVQMY9F88PCA)
* [了解帐户权限](https://advertising.amazon.com/help/GM4EFDQQPG9LGL3F)
* [Amazon Ads API权限](https://advertising.amazon.com/API/docs/en-us/guides/account-management/permissions)

## 为您的组织配置连接器 {#configure-organization}

管理员使[!DNL Amazon Ads]连接器对组织中的每个人可用。 组织页面上的更改适用于组织中的所有用户。 成员无法从&#x200B;**[!UICONTROL 用户]**&#x200B;作用域配置组织连接。

1. 打开&#x200B;**[!UICONTROL 自定义项]**，选择&#x200B;**[!UICONTROL 组织]**，然后选择&#x200B;**[!UICONTROL 外部连接器]**。 在&#x200B;**[!UICONTROL Amazon广告]**&#x200B;卡上，选择&#x200B;**[!UICONTROL 配置]**。

   将打开&#x200B;**[!UICONTROL 为您的组织配置Amazon广告]**&#x200B;对话框，其中包含&#x200B;**[!UICONTROL 连接详细信息]**、**[!UICONTROL 用户可用的工具]**&#x200B;以及&#x200B;**[!UICONTROL 访问和权限]**&#x200B;部分。 保存配置后，卡片显示&#x200B;**[!UICONTROL 已保存的配置]**，以及&#x200B;**[!UICONTROL 配置]**&#x200B;对&#x200B;**[!UICONTROL 查看配置]**&#x200B;的更改。

1. 在&#x200B;**[!UICONTROL Amazon广告区域]**&#x200B;下，选择与您的广告帐户匹配的区域。 Co-worker显示所选内容下区域的MCP服务器URL。

   | 区域 | MCP服务器URL |
   | --- | --- |
   | [!UICONTROL 北美洲]（默认） | `https://advertising-ai.amazon.com/mcp` |
   | [!UICONTROL 欧洲] | `https://advertising-ai-eu.amazon.com/mcp` |
   | [!UICONTROL 远东] | `https://advertising-ai-fe.amazon.com/mcp` |

   引导设置保存一个区域。 要稍后切换区域，请删除连接并重新进行设置。 然后，每个成员都需要再次登录，因此在中断工作连接之前规划更改。

1. Select **[!UICONTROL OAuth应用程序]**：

   * **[!UICONTROL Adobe管理的OAuth应用程序]：** Adobe提供了[!DNL Amazon Ads]应用程序，因此您无需输入应用程序凭据。 每个成员均使用自己的[!DNL Amazon]帐户登录并授权Adobe应用程序。

     ![使用北美地区、选定的Amazon管理的OAuth应用程序以及折叠的工具组为组织配置Adobe广告对话框。](./assets/amazon-ads/org-configure.png){width="500" zoomable="yes"}

   * **[!UICONTROL 使用我自己的OAuth应用程序]：**&#x200B;每个成员都使用自己的[!DNL Amazon]帐户授权您的组织应用程序。 在&#x200B;**[!UICONTROL 您的Amazon应用程序]**&#x200B;下，完成以下步骤：

     1. 确保在您的应用程序中注册了&#x200B;**[!UICONTROL 重定向URL]**。 有关详细信息，请参阅[注册重定向URL](#register-redirect-url)。
     1. 输入&#x200B;**[!UICONTROL Amazon应用程序ID]**&#x200B;和&#x200B;**[!UICONTROL Amazon应用程序密钥]**。 **[!UICONTROL Amazon应用程序ID]**&#x200B;字段采用OAuth客户端ID，而不是广告商ID、经理帐户ID或[!DNL Amazon]应用程序ID。 同事将您输入的值存储为组织密钥。
     1. 要改用已保存的凭据，请选择&#x200B;**[!UICONTROL 使用现有密码]**。 然后选择包含应用程序ID ]**的**[!UICONTROL &#x200B;密码和包含应用程序密码&#x200B;]**的**[!UICONTROL &#x200B;密码。 如果您的组织还没有密钥，请在&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 密钥]**&#x200B;中添加密钥。

     需要两个凭据。 仅在安全字段中输入凭据值。 请勿在纯值字段中输入机密引用。

1. 在&#x200B;**[!UICONTROL 用户可用的工具]**&#x200B;下，展开每个工具组并选择组织所需的工具。 默认情况下，仅选择`ads_accounts-list_ads_accounts`和`ads_accounts-get_ads_account`工具。 若要一次更改所有工具，请使用&#x200B;**[!UICONTROL Select all]**&#x200B;或&#x200B;**[!UICONTROL Clear all]**。 必须至少选择一个工具。

   从两个帐户工具开始，进行第一次访问检查。 Select campaign和报表工具仅在您的组织需要并批准它们时才可用。 有关详细信息，请参阅[工具组](#tool-groups)。

1. Select **[!UICONTROL 保存连接]**，然后查看保存的&#x200B;**[!UICONTROL amazon-ads]**&#x200B;连接器详细信息。

   | 设置 | 说明 |
   | --- | --- |
   | **[!UICONTROL Source]** | 所选区域的MCP服务器URL。 |
   | **[!UICONTROL 身份验证]** | 身份验证方法`amazon-ads_login`。 |
   | **[!UICONTROL 工具超时]** | Co-worker等待工具响应的时间。 |
   | **[!UICONTROL Connection]** | 正在使用的OAuth应用程序以及您自己的登录状态。 |
   | **[!UICONTROL 工具]** | 为成员选择的工具，具有&#x200B;**[!UICONTROL Select all]**&#x200B;和&#x200B;**[!UICONTROL Clear]**&#x200B;控件以及所选工具的计数。 |

   ![保存的amazon-ads连接器详细信息，其中显示北美来源、身份验证方法、一个与“注销”和“刷新”按钮关联的“已登录”，以及选定的47个工具中的两个。](./assets/amazon-ads/org-details.png){width="700" zoomable="yes"}

保存操作不会将您或任何成员登录到[!DNL Amazon]。 连接器详细信息中的&#x200B;**[!UICONTROL 连接]**&#x200B;状态是指您自己的连接，而不是与组织的连接。 要检查连接，请在连接器详细信息页面上选择&#x200B;**[!UICONTROL 登录]**&#x200B;以使用您自己的[!DNL Amazon]帐户登录，然后选择&#x200B;**[!UICONTROL 测试]**。 结果显示&#x200B;**[!UICONTROL 连接成功]**&#x200B;或&#x200B;**[!UICONTROL 连接失败]**，返回了工具或错误。 成功的结果不会确认对特定广告商操作的访问权限。

若要稍后更改成员可用的工具，请使用&#x200B;**[!UICONTROL Select全部]**&#x200B;或&#x200B;**[!UICONTROL 清除]**&#x200B;更新&#x200B;**[!UICONTROL 可用工具]**&#x200B;下的选择，然后选择&#x200B;**[!UICONTROL 保存工具选择]**。 必须至少保持选中一个工具。 成员无法更改工具选择。

要停止向您的组织提供连接器，请在连接器详细信息页面上选择&#x200B;**[!UICONTROL 删除]**。

### 工具组 {#tool-groups}

[!DNL Amazon Ads]连接器将其工具组织为以下组：

| 工具组 | 工具 | 工具的作用 |
| --- | --- | --- |
| [!UICONTROL 营销活动管理和定位] | 7 | 查询促销活动、广告组、广告、目标、项目组合及其关联，并检查产品资格。 |
| [!UICONTROL 帐户和组织] | 6 | 列出并获取广告帐户，查询广告商和帐户链接、经理帐户以及测试帐户。 |
| [!UICONTROL 用户访问和安全性] | 5 | 列出用户、角色、权限和邀请，然后获取邀请。 |
| [!UICONTROL 报告和分析] | 1 | 检索报表。 不包括报告创建。 |
| [!UICONTROL Amazon Marketing Cloud] | 6 | 读取工作流和数据源，以及现有执行的状态和下载URL。 不包括工作流执行。 |
| [!UICONTROL 帐单和财务摘要] | 4 | 读取发票、发票汇总、计费配置文件使用情况和计费通知。 |
| [!UICONTROL Amazon直播] | 12 | 读取频道、广播、直播、媒体、轮播和促销代码信息。 |
| [!UICONTROL 资格和优惠] | 6 | 阅读计划和产品资格、促销优惠和奖励以及术语令牌信息。 |

随着[!DNL Amazon]更新连接器，每个组中的工具都可以更改。 引导式设置会保存您选择的工具的精确列表，即使您选择了每个工具也是如此。 未选定的工具以及服务器以后添加的工具只有在您选择它们之后才能供成员使用。

>[!IMPORTANT]
>
>设置工具列表是为读取数据而策划的，但连接器作为整体不是只读的。 成员授权`advertising::campaign_management`范围，该范围比设置列表更广。 测试连接时，工具列表还可以包含服务器返回的工具。 在选择更多工具之前，请查看每个工具定义以及成员的[!DNL Amazon Ads]权限。

## 以成员身份登录 {#sign-in-as-a-member}

管理员配置连接器后，每个成员均使用自己的[!DNL Amazon]帐户登录。 您不需要应用程序密钥或访问令牌即可登录。

>[!NOTE]
>
>如果连接器指出您的环境中尚未提供该登录和&#x200B;**[!UICONTROL 测试]**，请在此处停止。 仅组织配置无法使成员登录可用。 联系您的 Adobe 代表。

1. 打开&#x200B;**[!UICONTROL 自定义项]**，选择&#x200B;**[!UICONTROL 用户]**，然后选择&#x200B;**[!UICONTROL 外部连接器]**。 查找&#x200B;**[!UICONTROL Amazon广告]**&#x200B;卡。

1. 如果卡片显示&#x200B;**[!UICONTROL 未配置]**，请要求您的管理员[配置连接器](#configure-organization)。 成员无法配置连接器。

1. 当卡片显示&#x200B;**[!UICONTROL 未登录]**&#x200B;时，选择&#x200B;**[!UICONTROL 登录]**。 允许登录弹出窗口，然后使用对您的广告帐户具有访问权限的[!DNL Amazon]帐户登录。

1. 完成[!DNL Amazon]身份验证提示，例如多重身份验证(MFA)和同意提示。 在批准之前，请查看应用程序名称和请求的访问权限。

   对于Adobe管理的应用程序，您可以授权Adobe应用程序。 对于您自己的组织应用程序，您可以改为授权该应用程序。

   >[!IMPORTANT]
   >
   >只有在您识别应用程序并且组织批准请求的访问权限时，才应继续。

1. 返回同事并确认卡片显示&#x200B;**[!UICONTROL 已登录]**。 Select **[!UICONTROL 查看详细信息]**，然后查看管理员启用的&#x200B;**[!UICONTROL 工具]**。 成员可以查看工具，但不能更改它们或删除组织连接。

1. Select **[!UICONTROL 测试]**&#x200B;以检查工具发现和连接状态。

仅关闭的弹出窗口并不确认登录成功。 成功的测试不会确认访问每个广告商、营销活动、报告或[!DNL Amazon Marketing Cloud]实例。 管理员登录时，其他成员未登录。

若要从连接器断开您的[!DNL Amazon]帐户，请选择&#x200B;**[!UICONTROL 注销]**。

## 检查您的广告帐户访问权限 {#check-account-access}

要确认您可以使用哪些广告帐户，请运行只读检查。 使用批准的测试帐户，并确保您的管理员启用了`ads_accounts-list_ads_accounts`和`ads_accounts-get_ads_account`工具。 然后，开始聊天并输入提示。

示例提示：

* “使用Amazon Ads，列出在配置的区域中，我最多可以访问5个广告帐户。 如果返回了帐户名称、帐户ID和区域，则仅显示这些字段。 请勿创建、更新、删除、启动、执行工作流、生成报告或更改权限。 如果列表限制不受支持，则仅汇总五个结果，并且不请求其他页面。”

确认结果包含您期望的帐户。 要查看更多详细信息，请让同事使用结果中的帐户ID获取该帐户的详细信息。 不要猜测帐户ID，也不要请求营销活动仅测试登录。

空的帐户列表并不总是意味着连接器无法正常工作。 检查您登录的[!DNL Amazon]帐户、接受的邀请、经理帐户所覆盖的链接广告商以及配置的区域。 没有营销活动的测试帐户也可以返回空营销活动列表。 如果您需要的工具未启用，请咨询您的管理员。 请勿使用更改数据的工具作为替代。

## 访问疑难解答 {#troubleshoot-access}

如果您无法访问您的[!DNL Amazon Ads]数据，请与管理员核对以下事项：

| 问题 | 检查内容 |
| --- | --- |
| **[!UICONTROL Amazon Ads]**&#x200B;卡或&#x200B;**[!UICONTROL Configure]**&#x200B;缺失 | 确认连接器对您的组织可用，并且您具有管理组织连接器的权限。 成员必须等待组织设置。 |
| Adobe管理的设置可保存，但登录失败 | 请联系您的Adobe代表，以确认在您的环境中可以使用由Adobe管理的应用程序。 成功保存不会确认这一点。 |
| 重定向URL不匹配 | 将Co-worker对话框中的完整&#x200B;**[!UICONTROL 重定向URL]**&#x200B;与[!DNL Login with Amazon]中的&#x200B;**[!UICONTROL 允许的返回URL]**&#x200B;进行比较，包括方案、主机和路径。 请勿使用来自其他MCP客户端、区域或环境的重定向URL，或者浏览器中同事页面的URL。 |
| **[!UICONTROL 重定向URL]**&#x200B;仅显示`/connectors/oauth/callback` | 您的环境尚未显示完整的重定向URL或支持登录和&#x200B;**[!UICONTROL 测试]**。 请勿注册部分路径或猜测主机名。 联系您的 Adobe 代表。 |
| 您无法保存自己的OAuth应用程序设置 | 输入OAuth客户端ID和客户端密钥，并至少选择一个工具。 确保&#x200B;**[!UICONTROL Amazon应用程序ID]**&#x200B;是OAuth客户端ID，而不是广告商ID或[!DNL Amazon]应用程序ID。 |
| 同意或应用程序授权失败 | 检查[!DNL Amazon Ads] API审批、安全配置文件、客户端ID和密码配对、重定向URL注册以及同意屏幕上显示的应用程序。 当您寻求帮助时，请勿共享同意URL、授权代码或令牌。 |
| 您已登录，但帐户或工具被拒绝或为空 | 检查您用来登录的[!DNL Amazon]帐户、接受的邀请、经理帐户涵盖的链接广告商、配置区域以及任务所需的权限。 对应用程序或合作伙伴工具的访问不会确认广告商访问权限。 [!DNL Amazon Marketing Cloud]访问权限是单独的。 |
| [!DNL Amazon Ads]说当前帐户无法访问页面 | Select **[!UICONTROL 更改帐户]**&#x200B;并选择广告商或经理帐户。 如果缺少帐户，请要求其管理员检查您是否接受了邀请，以及您是否被分配到帐户。 如果帐户存在但用户管理不可用，请要求管理员检查您的角色。 |
| 工具缺失或不可用 | 检查组织的工具选择、服务器返回的工具以及[!DNL Amazon Ads]权限。 服务器以后添加的工具不会自动选择。 默认情况下，仅启用这两个帐户工具。 |
| **[!UICONTROL 测试]**&#x200B;报告同名的个人连接器 | 同名的个人连接器可以优先于组织连接器。 按照所示的指南，仅删除或重命名冲突的个人连接器，并征得其所有者的同意。 |
| 登录弹出窗口被阻止、未完成或状态未更新 | 允许弹出窗口，然后返回同事以检查状态和任何错误详细信息。 请不要假定成功，因为弹出窗口已关闭或显示登陆页面。 |
| 工具超时，或者您必须重复登录 | 检查60秒&#x200B;**[!UICONTROL 工具超时]**、错误详细信息、网络和[!DNL Amazon]可用性以及应用程序配置。 |
| 同事说设置未启用，或者仍在设置新密码 | 与您的Adobe代表一起检查状态。 不要重复创建凭据，也不要将失败的存储视为成功。 |

联系支持人员时，请仅包含错误文本、错误时间、您的环境、所选区域和OAuth应用程序选项。 请勿共享应用程序密钥、访问令牌、授权代码、授权标头、同意或重定向查询参数，或客户帐户数据。
