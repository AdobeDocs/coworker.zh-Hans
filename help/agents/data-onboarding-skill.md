---
title: 与同事一起载入数据
description: 了解如何使用CX Coworker中的数据载入技能，通过对话工作流将新数据源载入到Adobe Experience Platform中。
hide: true
source-git-commit: 8f7d5307b1928c052f020ca5e7aae3feee7af03e
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 2%
---

# 与同事一起载入数据

>[!AVAILABILITY]
>
>数据载入技能处于测试阶段。 文档和功能可能会发生变化。
>
>数据载入技能适用于有权访问Adobe CX Enterprise Coworker的客户，您必须在其中为组织启用该技能。<!-- VERIFY BEFORE PUBLISH: confirm exact permission/entitlement name with Umesh Gohil, PLAT-296546. -->

使用CX Coworker中的数据载入技能，通过单个对话工作流将新数据载入到Adobe Experience Platform中。 您无需导航到多个屏幕来连接源并手动构建架构，而是可描述您的意图，由同事指导您完成源选择、数据质量、语义扩充、架构映射、架构创建和数据流创建。

<!-- VERIFY BEFORE PUBLISH: confirm the loaded skill name ("Onboard Data to Experience Platform") and the exact post-landing prompt/flow with Umesh Gohil once flag access is arranged. -->

## 先决条件 {#prerequisites}

在开始之前，请确保您具有：

- 访问Adobe Experience Platform以及相应的组织和沙盒。
- 访问Adobe CX Enterprise Coworker，并为您的组织启用Data Onboarding技能。
- 在Adobe Experience Platform中创建架构的权限。

有关安装插件的说明，请参阅[辅助进程UI指南](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)。

## 使用数据载入技能 {#use-the-data-onboarding-skill}

今天，数据载入技能开始于Experience Platform UI中的架构创建，这将打开已填写您意图的同事。

要使用数据载入技能，请执行以下操作：

1. 在Adobe Experience Platform中，导航到&#x200B;**[!UICONTROL 架构]**，然后选择&#x200B;**[!UICONTROL 创建架构]**。
1. 在&#x200B;**[!UICONTROL 创建架构]**&#x200B;对话框中，选择&#x200B;**[!UICONTROL 使用AI载入数据]**，然后选择&#x200B;**[!UICONTROL 选择]**。

   ![选择“使用AI创建板载数据”选项的“创建架构”对话框。](./assets/data-onboarding-skill/create-a-schema-dialog.png)

1. CX Coworker将在一个新的浏览器选项卡中打开，其中预填充了架构创建意图中的提示，因此您无需重新声明该提示。
1. 在出现提示时，选择要加入的源，例如[!DNL Amazon S3]、[!DNL Data Landing Zone]、[!DNL Delta Share]或[!DNL Marketo]。

   <!-- VERIFY BEFORE PUBLISH: screenshot of the Coworker landing/session-start state does not exist yet anywhere. Capture once flag access is confirmed. -->

1. 通过数据质量审查、语义扩充、架构映射和架构创建继续与同事对话，并随时确认每个步骤。

有关使用CX Coworker的更多信息，请参阅[同事UI指南](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)。

## 支持的用例 {#supported-use-cases}

探索载入工作流的各个部分。数据载入技能可帮助您完成。

### 选择并连接源

不要手动查找和配置源连接器，请描述您要引入的数据，让Co-worker帮助确定正确的源。

### 审查数据质量

在您提交到架构之前，Co-worker会为选定的源显示数据质量信号，以便您能够在该过程的早期发现问题。

### 在语义上丰富数据

Co-worker建议传入字段的语义含义，从而减少了将原始字段映射到标准定义的手动工作。

### 映射并创建架构

同事将审阅的字段映射到新的或现有的架构，并作为同一对话的一部分直接在Adobe Experience Platform中创建它。

### 创建数据流

同事通过创建持续导入数据所需的数据流来完成载入。

## 后续步骤 {#next-steps}

阅读本指南后，您应该了解如何从架构创建开始数据载入技能，以及它有助于您在CX Coworker中完成什么。

有关Experience Platform UI过程和访问/资格方案，请参阅架构UI指南中的[使用AI载入数据](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/ui/resources/schemas#data-onboarding-skill)。
