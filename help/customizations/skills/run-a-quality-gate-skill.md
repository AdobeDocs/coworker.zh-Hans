---
title: 在同事中培养并运行质量关卡技能
description: 了解如何使用自定义同事技能，在部署之前根据禁止列表、频率上限和命名标准自动验证受众激活。
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 101
last-substantial-update: 2026-09-08
jira: KT-22379
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%
---

# 使用自定义人工智能技能构建并运行质量关卡技能

营销团队依赖规则和治理流程来确保受众被正确激活。 在将受众启动到目标之前，团队通常需要验证禁止列表、频率限制、同意要求和命名约定。
 
挑战在于，这些检查往往取决于部落知识和人工审查。 当过程存在于人们的脑海中时，错误就可能发生。

在此视频中，您将了解自定义同事技能如何充当激活门，在受众向下游移动之前根据组织的激活标准自动验证受众。

>[!VIDEO](https://video.tv.adobe.com/v/3503162/?learn=on&enablevpops)

## 示例激活质量关卡技能
 
通过将提示粘贴到同事中，您可以创建自己的可重用**激活质量关卡**&#x200B;技能。 同事的技能创作功能将提示转换为&#x200B;**您自己的环境**内保存的技能。 下面是基于视频演示的示例。
 
关键是要为三个治理审核定义您自己的**通过/失败标准**：
 
1. 禁止/同意
2. 频率限制
3. 命名约定
 
每个人的框架都是一样的。 自定义标记为**`[...]`**&#x200B;的部分，以符合您组织的标准。

## 主提示

> **将此项另存为名为“激活质量关卡”的技能。**

```text
It's a governance gate that runs a pre-activation checklist before any audience is sent to a destination.

It is read-only. It never activates, mutates, or copies anything.

Resolve the named audience and destination from our Knowledge Graph, evaluate the three gates below, then render one visual scorecard containing:

- An Alert banner
- One MetricCard per gate
- A DataTable with:
- Gate
- Status
- Finding
- Required Fix

Provide a single verdict:

- CLEARED only if all three gates pass
- BLOCKED if any gate fails

For every failed gate, provide the specific remediation needed.
 
All gates fail closed:

- Missing data = BLOCKED
- Never assume success when information is unavailable
 
Trigger phrases:

- "run the activation gate"
- "is this audience ready to activate"
- "pre-activation checklist"
- "can I activate to ..."

The three gates are:
 
[Paste Gate 1, Gate 2, and Gate 3 definitions here]
```

## 入口1：禁止/同意
 
> 编辑此部分以符合您组织的禁止使用和同意要求。
 

```text
Gate 1 – Suppression List

Pass only if a recognized suppression, opt-out, or consent audience is applied alongside the target audience.

Discover eligible lists using name patterns such as:

- suppress
- opt-in
- opt out
- consent
- do not contact
 
Because suppression lists may live in destination dataflows rather than audience metadata, require the marketer to confirm one is attached.
 
If no suppression or consent list exists anywhere in the sandbox, fail hard.
 
Our standard:

[Example: A consent audience is mandatory for all email and SMS destinations. For direct mail destinations it is optional.]
```

## 门限2：频率限制

> 编辑此部分以匹配贵组织的投放频率要求。

```text
Gate 2 – Frequency Cap
 
Read the delivery frequency on the resolved destination.

Pass if:

- Frequency is present
- Frequency is bounded

Fail if:

- Frequency is blank
- Frequency is unbounded

Our standard:

[Example: Frequency must be DAILY or less frequent. Any hourly cadence or blank value is blocked.]
```

## 门3：命名约定
 
> 编辑此部分以匹配组织的受众命名规则。
 

```text
Gate 3 – Naming Convention

Evaluate the audience name programmatically.

Any rule violation causes failure.

Block names that:

- Contain "test"
- Contain "copy"
- Contain an auto-copy suffix such as _[6-hex]
- Contain timestamps
- Contain 24-character object IDs
- Start with a bare number or cryptic short code
- Are entirely lowercase
- Are excessively short or unclear
- Use generic defaults such as:
- Save audience
- Email
- New Accounts
- Lack a category–qualifier separator

Our standard:

[Example: [Line of Business] – [Criteria] in title case]

Example:

Mortgage – High Propensity Prospects

When blocked on naming, always propose a compliant replacement name.
```

## 指引

### &#x200B;1. 仅自定义带括号的部分

仅更新&#x200B;**`[...]`**中包含的部分。
 
这些部分定义了组织的特定治理标准。
 
其他一切都应保持不变：

- 受众解析
- 关口评估
- 记分卡渲染
- 判决逻辑


### &#x200B;2. 验证先决条件
 
此技能取决于：
 
- 知识图访问
- 受众发现
- 目标发现
- 禁止列表发现
- 可视化工件支持
- 警报横幅
- 量度卡片
- DataTable渲染

如果这些功能在客户的环境中不可用，则该技能将无法按设计要求运行。

### &#x200B;3. 将技能保持为只读

该技能应始终保持只读。

将此要求明确包含在提示中，以确保不会将技能与激活工作流混淆。

激活质量关卡仅评估激活准备情况。 它&#x200B;**不**&#x200B;激活受众、修改配置或复制数据。
