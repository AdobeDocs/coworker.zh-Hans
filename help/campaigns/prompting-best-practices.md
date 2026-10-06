---
description: 了解同事营销活动以提示最佳实践 — 联合启动框架、有无、不支持的内容以及提示的质量核对清单。
title: 提示最佳实践
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: ee66c1cc95ef1dd8c5e45c1fcb699547e63b9c8a
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 1%
---
# 提示最佳实践 {#best-practices}

要充分利用同事营销活动，首先需要您提供提示。 了解产生最佳结果的实践：用于构建提示的共星框架、要包含的内容和要避免的内容，以及基于情景的示例，这些示例为人工智能提供生成相关的目标内容所需的上下文。

>[!NOTE]
>
>目前，您只能连接到同事营销活动支持的集成。 如果您有任何现有的Adobe Enterprise应用程序（用于存储受众或构建历程），我们建议您改用[CX Enterprise Coworker](/help/chat/use-cases/overview.md)。

## 使用CO-STAR框架

为了获得最佳结果，请使用CO-STAR框架组织您的提示。 这种结构化方法可确保AI准确了解您所需的内容。

| 组件 | 它的含义 | 为什么这很重要 |
|-|-|-|
| **C — 上下文** | 有关营销活动、产品或情况的背景 | 帮助AI了解大局 |
| **O — 目标** | 您的特定营销目标 | 推动内容应实现的目标 |
| **S — 样式** | 您希望如何通信 | 设置方法 |
| **T — 音调** | 情感风格和声音 | 塑造您的信息感受 |
| **A — 受众** | 您定位的受众 | 确保消息与合适的人员引起共鸣 |
| **R — 要求** | 特定限制或必备项 | 定义边界和关键元素 |

## AI提示要点

### 做和不做

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Do</th>
<th>不要</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>使用CO-STAR框架进行结构</p>
<p>具有特定提取指南的焦点营销简述</p>
<p>绘制提示以产生所需的意图</p>
</td>
<td>
<p>在提示中要求进行结构更改、样式设置或图像编辑</p>
<p>使用“推广我们的产品”等含糊的说明</p>
<p>期待通过提示进行布局修改</p>
</td>
</tr>
</tbody>
</table>

### 提示中支持的内容

使用&#x200B;**电子邮件编辑器**&#x200B;或&#x200B;**Adobe Express**&#x200B;进行可视化/图像修改。 支持以下请求类型。

- **指定营销活动的频率和节奏**：“创建每周发送的电子邮件营销活动……”

- **从更大的列表中定位特定受众**：“仅针对那些带狗的与会者创建营销活动，以便在‘all-attendees.csv’中进行&#x200B;_公园里叫_&#x200B;活动”

- **上传HTML文件**：“使用我附加的HTML文件作为创建电子邮件促销活动的基础。”

- **在对话期间进行更改**：“将此营销活动结束前的天数从2天更改为3天。”

### 提示中不支持该内容

这些请求&#x200B;**不支持**，应通过其他工具处理：

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✗电子邮件结构修改</th>
<th>✗视化样式更改</th>
<th>编✗器内操作</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>选择要更改的特定部分</li>
<li>删除或克隆元素</li>
<li>条件选择</li>
<li>添加或删除布局部分</li>
</ul>
</td>
<td>
<ul>
<li>自定义字体</li>
<li>颜色修改</li>
<li>布局样式（边框、填充、边距）</li>
<li>视觉效果（阴影）</li>
</ul>
</td>
<td>
<ul>
<li>背景更改</li>
<li>添加文本叠加图或徽标</li>
<li>图像裁剪或调整大小</li>
<li>颜色调整</li>
</ul>
</td>
</tr>
</tbody>
</table>

### 质量核对清单

在生成内容之前，请确保满足以下条件：

✓ **清除目标**：清楚地声明操作、产品/服务、值和上下文。

✓ **已定义目标受众**：指定人口统计、角色或区段。

✓ **将正确的品牌指定为默认值**：选择了适当的品牌准则。

✓ **实际范围**：避免请求布局更改、样式或结构编辑。

## 基于方案的提示示例

始终提供上下文和价值主张，以便AI可生成相关内容。

>[!NOTE]
>
>虽然您当前只能生成和启动电子邮件营销活动，但始终可以要求同事为社交媒体、WhatsApp或短信生成副本。

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>行业</th>
<th>示例提示</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B技术</strong></td>
<td>“创建四点接触式电子邮件促销活动，展示ROI和技术规范，同时帮助IT决策者评估我们的云基础架构解决方案以解决安全问题，其中重点是99.9%的正常运行时间、符合SOC 2的要求以及40%的成本节约。”</td>
</tr>
<tr>
<td><strong>电子商务零售</strong></td>
<td>“推出单次接触式促销活动，以紧急应对库存有限的节日商品，同时强调免运费和方便最后一刻购物者的退货，并强调数量有限（剩余50件不到）和24小时发货截止时间。”</td>
</tr>
<tr>
<td><strong>教育和培训</strong></td>
<td>“创建一项强调职业发展成果和行业认证的双接触式营销活动，同时展示讲师的专业知识，突出显示92%的职位安排率和基于项目的课程。”</td>
</tr>
<tr>
<td><strong>咨询</strong></td>
<td>“通过展示三个具有详细ROI标准的客户成功案例（IBM：成本降低45%，Accenture：潜在客户增长200%，Microsoft：时间节省60%），开展三点营销活动以培育企业潜在客户，面向拥有1000多名员工的企业的IT主管。”</td>
</tr>
</tbody>
</table>

## 一般营销提示想法

### 内容营销

- “制作20个博客主题，回答首次购房者的常见问题。”
- “LinkedIn集思广益，为创建B2B网络安全初创公司提出想法。”
- “创建一个为期三个月的内容日历，专注于培训新客户。”
- “建议可重新用于博客、视频、新闻稿和社交帖子的内容主题。”

### 电子邮件营销

- “为对可持续时尚感兴趣的新订阅者生成欢迎电子邮件序列。”
- “脑力激荡主题线，它们创造好奇心，但听起来不像点击诱饵。”
- “针对不活跃的客户提出重新接触促销活动建议。”
- “为已完成入门培训的用户创建生命周期电子邮件想法。”

>[!MORELIKETHIS]
>
>浏览更多[协同工作营销活动的提示模式](use-cases.md)。
