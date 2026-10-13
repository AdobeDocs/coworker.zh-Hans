---
source-git-commit: e5bf2a0a2ee55513b32442f70d01dc5825ac9d6a
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%
---
# CX Enterprise Coworker 文档

适用于Adobe CX Enterprise Coworker文档集的Source 。

## 发布配置

在`.github/workflows/`中使用共享文章验证和镜像工作流。
验证工作流针对拉取请求运行，并推送到`main`。
当您推送到`main`时，镜像工作流将运行。

将`markdownlint_custom.json`用于Markdown规则覆盖，并将`linkcheckexclude.json`用于URL排除示例。
`pipeline.opts`文件遵循`cx-enterprise-ai.en`中的链接检查配置。
使用`source,dest`列添加URL重定向到`redirects.csv`。
