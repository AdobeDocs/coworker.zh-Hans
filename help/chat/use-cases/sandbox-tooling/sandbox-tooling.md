---
title: 沙盒工具代理技能
description: 了解如何使用沙盒工具代理技能跨沙盒环境复制对象元数据。
source-git-commit: 8e60434a3ede23f916aa57667d1cec9186386e61
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 1%
---

# 沙盒工具代理技能

>[!AVAILABILITY]
>
>所有有权访问Adobe CX Enterprise Coworker的客户都可以获得沙盒工具代理技能。 要使用所有可用功能，您需要以下权限：
>
>**Manage-sandbox**&#x200B;或&#x200B;**View-sandbox**：这些权限允许您使用Sandbox Tooling Agentic Skills直接在Co-worker中查看沙盒。
>
>**Manage-package**：此权限允许您使用Sandbox Tooling Agentic Skills直接在同事中创建包。

使用沙盒工具代理技能，通过以自然语言描述要完成的任务来跨Adobe Experience Platform环境移动支持的对象类型。 使用协同工作，您可以发现所需的元数据、自动识别依赖项、创建迁移包以及通过对话体验迁移对象。

>[!VIDEO](https://video.tv.adobe.com/v/3496706?learn=on)

## 先决条件 {#prerequisites}

在开始之前，请确保您具有：

- 访问Adobe Experience Platform以及相应的组织和沙盒。
- 访问要发现或迁移的对象。
- 安装在同事中的Adobe CXO插件。

有关安装插件的说明，请参阅[辅助进程UI指南](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)。

## 使用沙盒工具代理技能 {#use-sandbox-tooling-agentic-skills}

通过同事使用自然语言与沙盒工具代理技能交互。 尽可能清楚地描述您的目标。 特定请求会产生最佳结果，而模糊或过于短暂的提示可能会返回质量较低的结果，或者不会调用代理。

要使用沙盒工具代理技能，请执行以下操作：

1. 导航到&#x200B;**[!UICONTROL CX Coworker]**。
1. 输入要完成的任务的明确说明。 例如：

   *“将架构忠诚度会员白金从当前沙盒移动到Acme演示沙盒。”*

1. 查看结果表，其中显示了源沙箱和目标沙箱。 准备好继续时，选择&#x200B;**[!UICONTROL 继续]**，然后选择&#x200B;**[!UICONTROL 提交]**&#x200B;以进行确认。

   ![选择“继续”的请求结果，突出显示“提交”。](./assets/sandbox-tooling/results-proceed.png)

1. 选择要迁移的一个或多个对象，然后选择&#x200B;**[!UICONTROL 提交]**。

   ![对象选择页面突出显示Submit。](./assets/sandbox-tooling/object-selection.png)

1. 查看代理标识的对象和依赖项，并确认操作操作 — *新建*&#x200B;或&#x200B;*使用现有*。 准备开始迁移时，请选择&#x200B;**[!UICONTROL 继续]**，然后选择&#x200B;**[!UICONTROL 提交]**&#x200B;进行确认。 迁移可能需要几分钟才能完成。

   ![确认行动计划页面突出显示“提交”。](./assets/sandbox-tooling/action-plan.png)

1. 迁移完成后，所选对象将在目标沙盒中可用。

   ![显示请求状态的“传输完成”页面。](./assets/sandbox-tooling/transfer-complete.png)

有关使用同事的详细信息，请参阅[同事用户界面指南](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)。

## 支持的用例 {#supported-use-cases}

探索使用沙盒工具代理技能简化沙盒管理和元数据迁移的常见方法。

### 在沙盒之间移动对象元数据

作为管理多个Adobe Experience Platform沙盒的沙盒管理员，您可以使用自然语言请求迁移对象元数据，而不是手动导航用户界面。

使用同事，您可以通过用自然语言描述迁移过程，将受支持的Adobe Experience Platform对象及其关联的元数据从一个沙盒迁移到另一个沙盒。 沙盒工具代理技能可自动识别依赖项，打包所需对象，并帮助确保跨环境的可靠迁移。

例如：

- “将架构Luma忠诚度会员白金从当前沙盒移动到生产沙盒。”

### 将对象提升到多个沙箱(Beta)

>[!NOTE]
>
>多沙盒管理当前位于Beta中，仅支持架构和数据集。

作为沙盒管理员，您可以在单个工作流中将受支持的对象从源沙盒提升到多个目标沙盒。 使用同事选择目标沙盒、审查建议的更改以及在各个环境中以一致的方式部署配置，而不是将包单独导入每个沙盒中。 多沙盒管理会自动解析依赖关系，并在升级开始之前提供更改预览。

例如：

- “将忠诚度成员架构提升到所有区域沙箱。”

### 在沙盒之间提升受众

作为沙盒管理员，您可以在环境之间提升受众，而无需手动重新创建或重新配置受众。

例如：

- “将‘受众名称’受众提升到暂存沙盒。”

沙盒工具代理技能识别指定的受众，验证其依赖关系，并将所有必需对象迁移到目标沙盒。

## 示例提示 {#example-prompts}

使用下列提示作为与“沙盒工具代理技能”交互时的示例。

### 架构提示

当您知道架构名称和目标沙盒时，请使用这些提示。

- “将架构‘架构名称’从当前沙盒移动到生产沙盒。”

### 受众提示

当您知道受众名称时，可以使用这些提示。

- “将‘受众名称’受众提升到暂存沙盒。”

## 后续步骤 {#next-steps}

阅读本指南后，您应该了解如何使用沙盒工具代理技能在沙盒之间发现、打包和迁移受支持的对象。

有关沙盒工具的详细信息，请参阅[沙盒工具指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sandbox/ui/sandbox-tooling)。

