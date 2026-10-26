---
description: 了解如何打开同事聊天、设置组织和沙盒、发送第一条消息以及自定义技能、集成服务器和内存。
title: 同事聊天入门
jira: KT-22106
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: d611ce2398cba72cf21c766f3b25225765c1675b
workflow-type: tm+mt
source-wordcount: '1902'
ht-degree: 2%
---
# 同事聊天入门 {#ui-guide}

同事聊天功能允许您以简单的语言询问所需的内容，从而使用Adobe CX Enterprise数据和工具。 使用此页面打开“同事聊天”，发送您的第一条消息，并设置您的工作方式。

## 可用性

[!DNL Coworker] [!UICONTROL 聊天]可用作沉浸式体验、全页工作区以及某些[!DNL CX Enterprise]应用程序中的产品内体验。

下表显示了每个体验的可用位置。

| CX Enterprise应用程序 | 沉浸式体验 | 产品内体验 |
|---|---|---|
| Real-Time CDP | 现在可用 | 即将推出 |
| Adobe Journey Optimizer | 现在可用 | 即将推出 |
| Customer Journey Analytics | 现在可用 | 即将推出 |
| Workfront | 现在可用 | 现在可用 |
| 目标 | 现在可用 | 现在可用 |
| AEM | 现在可用 | 现在可用 |
| Marketo Engage | 现在可用 | 即将推出 |

## 打开[!DNL Coworker]聊天 {#immersive}

要使用沉浸式体验，请使用您的Adobe凭据登录。 您可以通过直接链接或在CX Enterprise中打开它。

1. 转到[https://experience.adobe.com/#/coworker](https://experience.adobe.com/#/coworker)。
1. 使用您的 Adobe ID 登录。
1. 在[!DNL CX Enterprise]中，单击应用程序选择器菜单![产品菜单图标](./assets/apps-icon.png)，然后单击&#x200B;**[!DNL Coworker]**。
1. 要打开“聊天”（产品内体验），请单击&#x200B;**[!UICONTROL 聊天]**![同事图标](./assets/icon-coworker.png)。

CX Enterprise应用程序选择器中的![同事](./assets/ui-guide-1.png)

## 视频 — [!DNL Coworker]聊天界面的基础知识

>[!VIDEO](https://video.tv.adobe.com/v/3498575?captions=chi_hans&learn=on)

## 选择您的组织

您的[组织](https://experienceleague.adobe.com/zh-hans/docs/core-services/interface/administration/organizations)和沙盒决定了对话可以联系的数据、技能和连接工具。 开始前请检查。 当前上下文显示在左侧导航器边栏的底部，且位于您的名称下方。

要更改上下文，请执行以下操作：

1. 单击导航边栏底部的您的姓名以打开帐户菜单。
1. 单击&#x200B;**[!UICONTROL 组织]**，然后选择要使用的IMS组织。

   ![组织选取器打开的帐户菜单](./assets/ui-guide-2.png)

1. 单击&#x200B;**[!UICONTROL 沙盒]**，然后选择要使用的AEP沙盒。

   ![打开了沙盒选取器的帐户菜单](./assets/ui-guide-3.png)

帐户菜单还包括以下选项：

| 选项 | 使用它可以 |
| --- | --- |
| **[!UICONTROL 主题]** | 在浅色和深色主题之间切换。 |
| **[!UICONTROL 设置]** | 查看帐户详细信息和工作区设置。 |
| **[!UICONTROL CX应用程序]** | 转到与您的帐户连接的其他CX Enterprise应用程序。 |
| **[!UICONTROL 注销]** | 注销您的Adobe帐户。 |

## 找到路来

工作区有两个区域：左侧的导航边栏和填充窗口其余部分的对话画布。

![主屏幕](./assets/ui-guide-4.png)

使用导航边栏在产品的各个部分之间移动并返回最近工作。

| 选项 | 使用它可以 |
| --- | --- |
| **[!UICONTROL 新聊天]** | 开始对话。 同事聊天会将您当前的聊天保存到历史记录中。 |
| **[!UICONTROL 主页]** | 返回问候语、输入框和建议的提示。 |
| **[!UICONTROL 聊天]** | 搜索、固定、存档或删除过去的对话。 |
| **[!UICONTROL 自定义项]** | 管理技能、集成、市场、插件和内存。 |
| **[!UICONTROL 已固定]** | 打开你主演的对话。 单击&#x200B;**[!UICONTROL 查看全部]**&#x200B;可在“聊天”页面上查看它们。 |
| **[!UICONTROL 最近访问]** | 打开您的最新对话。 单击&#x200B;**[!UICONTROL 查看全部]**&#x200B;以打开“聊天”页面。 |

## 发送您的第一条消息

主屏幕显示问候语、输入（[!UICONTROL 聊天]）框以及根据同事聊天在沙盒中可以执行的操作而建议的提示。 您可以从建议开始，也可以编写您自己的消息。

要发送消息：

1. 单击导航边栏中的&#x200B;**[!UICONTROL 主页]**。
1. 执行以下操作之一：

   * 在&#x200B;**[!UICONTROL “为您建议”]**&#x200B;下选择一个提示。 Co-worker Chat将其添加到输入框中，您可以在其中编辑它。
   * 在&#x200B;**[!UICONTROL 向同事询问任何内容]**&#x200B;框中输入您自己的请求。

1. （可选）添加上下文，选择同事聊天如何响应或听写您的消息。 请参阅[添加上下文并选择响应样式](#input-options)。
1. 单击&#x200B;**[!UICONTROL 发送]**。

>[!TIP]
>
>建议的提示将显示同事聊天支持的任务类型，例如在沙盒之间移动架构、在历程中发现异常以及验证数据集。

若要将Co-worker Chat指向沙盒中的特定对象，请在输入框中键入&#x200B;**+**，然后单击架构、历程、数据集或其他对象。 这叫做实体提及。 它会告诉同事聊天确切地说您指的是哪个对象。

## 添加上下文并选择响应样式 {#input-options}

输入框下方的工具栏控制您附加的内容、“同事聊天”处理任务的方式以及您看到的任务的工作量。

| 控件 | 使用它可以 |
| --- | --- |
| **[!UICONTROL +]**（附加） | 向消息中添加文件或沙盒对象。 |
| **[!UICONTROL 计划模式]** | 在同事聊天采取行动之前，查看分步计划。 |
| **[!UICONTROL 成绩单视图]** | 选择您看到的“同事聊天”活动量。 |
| **[!UICONTROL 麦克风]** | 听写您的留言。 再次单击以停止录制。 |
| **[!UICONTROL 发送]** | 发送您的消息。 Co-worker Chat响应时，此控件将变为&#x200B;**[!UICONTROL Stop]**，从而中断响应。 |

### 附加文件或对象

当同事聊天需要更多信息来完成工作时，附加文件或对象。

1. 在输入框中单击&#x200B;**[!UICONTROL +]**。
1. 单击下列选项之一：

   * **[!UICONTROL 附加文件]**：上载一个供同事聊天阅读和参考的文件。
   * **[!UICONTROL 添加数据或对象]**：引用沙盒中的对象，如数据集或架构，因此Co-worker Chat对您的实时数据有效。

![附加菜单](./assets/ui-guide-5.png)

### 在同事聊天采取行动之前查看计划 {#plan-mode}

对于更改数据的复杂任务或任务，请使用“计划”模式。 当“计划”模式打开时，“同事聊天”会提出计划并等待您的批准，然后才执行计划。 当“计划”模式关闭时，“同事聊天”会立即开始工作。

1. 单击输入工具栏中的&#x200B;**[!UICONTROL 计划模式]**&#x200B;以将其打开。
1. 发送您的消息。
1. 审查计划并批准它以继续。

![在输入工具栏中打开了计划模式](./assets/ui-guide-6.png)

### 选择成绩单视图

成绩单视图控制了Co-worker Chat的推理和工具活动在对话中的显示量。

1. 单击输入工具栏中的&#x200B;**[!UICONTROL 成绩单视图]**。
1. 单击视图：

   | 查看 | 您所看到的内容 |
   | --- | --- |
   | **[!UICONTROL 正常]** | 关键思维步骤和工具活动的摘要。 |
   | **[!UICONTROL 焦点]** | 大部分是答案。 同事聊天会隐藏大多数中间步骤。 |
   | **[!UICONTROL 详细]** | 每个思考步骤、技能载入、文件读取和查询。 |

![成绩单视图选项](./assets/ui-guide-7.png)

## 查看响应

Chat同事会实时显示其工作，然后返回答案。 响应可能包括其推理、所用工具的记录、工件和摘要。

![响应正在进行中](./assets/ui-guide-8.png)

### 关注活动

在“同事聊天”工作期间，您可以关注并验证其功能。 展开任意条目以查看更多详细信息。

* **考虑对象**：包含同事聊天推理的可折叠块以及所用时间。
* **已加载的技能**：用于任务的专用功能同事聊天。
* **读取文件**&#x200B;和&#x200B;**已运行1个查询**： Co-worker Chat读取的文件和已运行的查询，以及每个查询所用的时间。

>[!TIP]
>
>将&#x200B;**[!UICONTROL 成绩单视图]**&#x200B;设置为&#x200B;**[!UICONTROL 详细]**&#x200B;以查看每个步骤，或设置为&#x200B;**[!UICONTROL 集中]**&#x200B;以隐藏每个步骤。

### 使用工件

“同事聊天”将结果（如受众表）显示为响应中的工件卡。 您可以从表工件的信息卡中以CSV文件格式下载表工件。 如果响应包含多个项目，请使用&#x200B;**[!UICONTROL Previous]**&#x200B;和&#x200B;**[!UICONTROL Next]**&#x200B;在它们之间移动。

### 使用摘要

在工件下方，同事聊天将说明结果的含义，突出显示重要调查结果，并建议后续操作。 使用这些建议继续对话。

![具有工件表和摘要的已完成响应](./assets/ui-guide-9.png)

### 评级和复制响应

每个响应都包含可用于提供反馈或重用内容的控件。

* 单击&#x200B;**[!UICONTROL 向上缩略图]**&#x200B;或&#x200B;**[!UICONTROL 向下缩略图]**&#x200B;对响应进行评级。 您的评级有助于改进未来的答案。
* 单击&#x200B;**[!UICONTROL 复制]**，然后选择&#x200B;**[!UICONTROL 复制为Markdown]**&#x200B;以保留格式，或者选择&#x200B;**[!UICONTROL 复制为纯文本]**&#x200B;以将其删除。

![复制菜单](./assets/ui-guide-10.png)

## 管理您的聊天

您的聊天历史记录会保留过去的对话，以便您能够返回这些对话。 单击导航边栏中的&#x200B;**[!UICONTROL 聊天]**&#x200B;以将其打开。 对话按日期分组，每一行显示标题和轮次数。

![聊天页面](./assets/ui-guide-11.png)

在“聊天”页面上，您可以：

* 在&#x200B;**[!UICONTROL 按标题搜索]**&#x200B;中输入名称以查找对话。
* 单击&#x200B;**[!UICONTROL 显示固定]**&#x200B;以仅查看您收看的对话。
* 单击&#x200B;**[!UICONTROL 显示已存档的]**&#x200B;以查看已存档的对话。
* 单击&#x200B;**[!UICONTROL 新建聊天]**&#x200B;开始对话。

若要固定、重命名、存档或删除对话，请单击对话行上的行菜单(**[!UICONTROL ...]**)并选择选项。

## 自定义同事聊天

[!UICONTROL 自定义项]是您控制[!UICONTROL 同事聊天]功能的地方。 单击导航边栏中的&#x200B;**[!UICONTROL 自定义项]**，然后选择选项卡： **[!UICONTROL 技能]**、**[!UICONTROL 集成]**、**[!UICONTROL 市场]**、**[!UICONTROL 插件]**&#x200B;或&#x200B;**[!UICONTROL 内存]**。

### 添加和查看技能

技能是“同事聊天”在应用时自动使用的专用功能。 您也可以在聊天中键入&#x200B;**/**&#x200B;以自己开始一项技能。 “**[!UICONTROL 技能]**”选项卡列出了所有已安装的技能。

![技能选项卡](./assets/ui-guide-12.png)

1. 在&#x200B;**[!UICONTROL 技能]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 添加技能]**&#x200B;以从新来源安装技能。
1. 在&#x200B;**[!UICONTROL 搜索]**&#x200B;中输入名称以查找技能。
使用视图切换可在网格和列表布局之间切换。
1. 选择一种技能，以查看Co-worker Chat使用插件时该插件所属的插件及其包含的文件。

   ![显示支持文件的技能详细信息视图](./assets/ui-guide-13.png)

1. （可选）单击&#x200B;**[!UICONTROL 查看SKILL.md]**&#x200B;阅读完整的技能定义，或单击&#x200B;**[!UICONTROL 删除Source]**&#x200B;卸载技能。

   ![SKILL.md查看器](./assets/ui-guide-14.png)

### 连接服务器 {#server}

Server A集成将同事聊天连接到外部工具和服务，例如Adobe Journey Optimizer、Real-Time CDP、Target和Workfront。 **[!UICONTROL 自定义项]** > **[!UICONTROL 用户]** > **[!UICONTROL 集成]**&#x200B;选项卡列出了已连接的服务器和活动连接数。 每个信息卡都会显示服务器名称、其端点，以及描述其所提供内容的标记。

1. 导航到&#x200B;**[!UICONTROL 自定义项]** > **[!UICONTROL 用户]** > **[!UICONTROL 集成]**

   ![服务器选项卡](./assets/get-started-customizations.png)

1. 在自定义项上，单击&#x200B;**[!UICONTROL 添加服务器]**。

   ![添加集成](./assets/get-started-add-integrations.png)

1. 填写以下字段和选项：

   * **[!UICONTROL 服务器名称]**（必需）：输入可在集成列表中标识该服务器的名称，例如`github`或`slack`。
   * **[!UICONTROL Source URL或命令]**（必需）：输入同事聊天连接的地址，例如`https://mcp.example.com/sse`。
   * **[!UICONTROL 连接类型]**：选择服务器用于与同事聊天进行通信的协议： **[!UICONTROL SSE]**（服务器发送的事件）或&#x200B;**[!UICONTROL HTTP]**。 默认值为&#x200B;**[!UICONTROL SSE]**。
   * **[!UICONTROL 工具超时（秒）]**：设置同事聊天在此服务器上等待工具响应的时间，然后停止请求。 默认值为60秒。
   * **[!UICONTROL 身份验证]**：选择Co-worker Chat向服务器证明其身份的方式。 默认值为&#x200B;**[!UICONTROL 无]**，它不发送任何凭据。 如果服务器需要凭据，请选择其他方法。
   * **[!UICONTROL 标头]**：单击&#x200B;**[!UICONTROL 添加标头]**&#x200B;将每个请求都发送到服务器时额外的HTTP标头（如API密钥）。 此选项是可选的。

1. 单击&#x200B;**[!UICONTROL 添加]**。

### 添加市场

Marketplace是插件的注册表，您可以从中浏览和安装。 在&#x200B;**[!UICONTROL 市场]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 添加市场]**&#x200B;以注册一个新市场。 使用&#x200B;**[!UICONTROL 搜索]**&#x200B;或按组筛选以缩小列表范围。 状态为&#x200B;**就绪**&#x200B;的商城可供安装。

![Marketplaces选项卡](./assets/ui-guide-16.png)

### 管理插件

插件将技能和服务器捆绑在一起，以便您能够一起安装和管理它们。 **[!UICONTROL 插件]**&#x200B;选项卡显示已安装的插件。

* 单击&#x200B;**[!UICONTROL 浏览市场]**&#x200B;以查找新插件。
* 按市场筛选，以查看每个插件的来源。
* 单击&#x200B;**[!UICONTROL 卸载]**&#x200B;可删除插件及其捆绑的所有内容。

![插件选项卡](./assets/ui-guide-17.png)

### 管理内存

内存让同事聊天可以记住您在不同对话中的首选项，因此随着时间的流逝，响应将保持相关性。 使用&#x200B;**[!UICONTROL 内存]**&#x200B;选项卡控制保留的内容。

1. 在“自定义项”页面上单击&#x200B;**[!UICONTROL 内存]**。
1. 打开&#x200B;**[!UICONTROL 启用内存]**。 将其关闭以阻止跨会话记住同事聊天。
1. 在&#x200B;**[!UICONTROL 存储的首选项]**&#x200B;下，查看保存了哪些同事聊天。 您可以编辑、删除或检查每个条目，并按类别筛选条目。
1. 使用&#x200B;**[!UICONTROL 保存的记忆历史记录]**&#x200B;查看记忆更改的时间表。

![内存选项卡](./assets/ui-guide-18.png)
