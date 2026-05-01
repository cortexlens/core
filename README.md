<p align="center">
  <strong>安全威胁态势实时感知系统</strong>
</p>

<p align="center">
  <a href="https://github.com/cortexlens/core/releases"><img src="https://img.shields.io/badge/version-0.1.0--alpha-blue" alt="Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-Apache%202.0-green" alt="License"></a>
  <a href="https://go.dev"><img src="https://img.shields.io/badge/go-1.22%2B-00ADD8?logo=go" alt="Go Version"></a>
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen" alt="PRs Welcome"></a>
  <a href="https://discord.gg/cortexlens"><img src="https://img.shields.io/badge/discord-join%20chat-5865F2?logo=discord" alt="Discord"></a>
</p>

<p align="center">
  <a href="#-项目简介">项目简介</a> •
  <a href="#-为什么选择-cortexlens">为什么选择</a> •
  <a href="#-核心特性">核心特性</a> •
  <a href="#-与竞品对比">竞品对比</a> •
  <a href="#-快速开始">快速开始</a> •
  <a href="#-架构概览">架构概览</a> •
  <a href="#-内置检测能力">检测能力</a> •
  <a href="#-文档">文档</a> •
  <a href="#-社区">社区</a> •
  <a href="#-路线图">路线图</a> •
  <a href="#-许可证">许可证</a>
</p>

---

## 📖 项目简介

**CortexLens** 是一套基于 Go 语言开发的开源安全威胁态势实时感知系统。

> **Cortex** = 大脑皮层（智能分析核心）  
> **Lens** = 透镜（精准洞察之眼）  
> **CortexLens** = 安全智能的洞察之眼

### 我们解决的问题

对于 **200-2000 人**的企业或机构：

| 痛点                                                 | CortexLens 方案                                    |
| ---------------------------------------------------- | -------------------------------------------------- |
| ❌ Splunk / Palo Alto Cortex XSIAM 太贵（$50万/年起） | ✅ 开源核心免费，企业版 $5,000-$50,000/年           |
| ❌ Wazuh / Security Onion 部署复杂、实时性弱          | ✅ Docker Compose 一键部署，5 分钟上线              |
| ❌ ELK + 自研规则缺少开箱即用安全能力                 | ✅ 内置 200+ 检测规则，兼容 Sigma 和 Falco 社区规则 |
| ❌ 招不到专职安全分析师                               | ✅ AI 原生分析引擎，LLM 自动摘要和研判              |

**一句话定位：**

> **CortexLens = Wazuh 的全面性 + Falco 的内核级深度 + 原生 AI 智能分析 + Go 语言的极致性能，全部打包进一个 Docker Compose 里。**

---

## 🎯 为什么选择 CortexLens？

### 当前开源安全生态的空白

| 项目                 | 定位               | 短板                                            |
| -------------------- | ------------------ | ----------------------------------------------- |
| **Wazuh**            | 开源 SIEM + XDR    | C+Python 架构老旧，非实时，无 AI，部署复杂      |
| **Falco**            | 云原生运行时安全   | 纯系统调用监控，无日志分析，无 SIEM，无 AI      |
| **Security Onion**   | 全栈安全监控发行版 | 组件多达 10+ 个，8 核 16GB 起步，运维极复杂     |
| **UTMStack**         | 统一威胁管理       | Java 技术栈，社区弱小（200+ Star），无原生 AI   |
| **ELK + ElastAlert** | 自建日志分析       | 无开箱安全能力，ElastAlert 基于 Python 2 性能差 |

### CortexLens 独有优势

| 优势                 | 说明                                                         |
| -------------------- | ------------------------------------------------------------ |
| 🏗️ **架构代际领先**   | Go 全栈统一，单节点 50,000+ EPS，比 Python/Java 方案高 5-10 倍 |
| 🔄 **双引擎互补**     | **业内唯一**同时原生兼容 Sigma 规则（日志层）和 Falco 规则（内核层）的开源项目 |
| 🧠 **AI 原生能力**    | 8 套预置安全分析提示词模板，支持 OpenAI / DeepSeek / Ollama 等可插拔模型 |
| 🪶 **极致轻量**       | 单二进制交付，2 核 4GB 全功能运行，Docker Compose 一键部署   |
| 🔌 **社区规则复用**   | 完全兼容 Sigma + Falco 社区数千条规则，**不用重复造轮子**    |
| 🔍 **内核级资产发现** | eBPF 无侵入监控 + 服务指纹识别，自动识别 Nginx/MySQL/Redis 等所有服务 |
| 📊 **真·开箱即用**    | 下载即能发现问题，内置 200+ 规则 + Grafana 态势大屏          |

---

## ✨ 核心特性

| 特性                   | 说明                                                         |
| ---------------------- | ------------------------------------------------------------ |
| ⚡ **高性能实时流处理** | Go 原生并发 + 流式管道，单节点 50,000+ EPS，端到端延迟 < 1 秒 |
| 🪶 **极致轻量化**       | 单二进制交付，最小 2 核 4GB 即可运行                         |
| 🧠 **AI 原生分析**      | LLM Gateway 可插拔模型架构，预置 8 套安全分析提示词模板      |
| 🎯 **双引擎威胁检测**   | 原生兼容 Sigma 规则 + Falco 规则，200+ 内置规则              |
| 🔗 **智能关联分析**     | 序列 / 统计 / 资产 / 情报四维关联，自动聚合安全事件          |
| 🤖 **SOAR 自动化响应**  | Temporal 工作流引擎，预置 20+ 响应剧本                       |
| 🔍 **内核级资产发现**   | eBPF 深度监控 + 服务指纹自动识别                             |
| 📊 **态势感知大屏**     | Grafana 集成 + React 控制台，攻击地图、ATT&CK 热力图         |
| 🔒 **安全通信**         | mTLS 服务间认证，数据加密传输                                |
| 🐳 **Docker 一键部署**  | 5 分钟从零到完整运行                                         |

---

## 🆚 与竞品对比

### 核心架构

| 维度          | Wazuh          | Security Onion   | Falco              | **CortexLens**                     |
| ------------- | -------------- | ---------------- | ------------------ | ---------------------------------- |
| 开发语言      | C+Python       | 多语言混搭       | C++/Go             | **Go 1.22+ 全栈统一**              |
| 最低配置      | 4-8 核，8-16GB | 8-16 核，16-32GB | 2 核 4GB（仅检测） | **2 核 4GB（全功能）**             |
| 单节点 EPS    | 5,000-10,000   | 10,000-20,000    | N/A                | **50,000+**                        |
| eBPF 深度监控 | 有限           | 无               | ✅ 核心             | **✅ 全链路**                       |
| 实时性        | 分钟级         | 分钟级           | 毫秒级             | **毫秒级（eBPF）+ 秒级（流处理）** |

### AI 能力（核心差异）

| 维度         | Wazuh | Security Onion | Falco | UTMStack     | **CortexLens**                        |
| ------------ | ----- | -------------- | ----- | ------------ | ------------------------------------- |
| AI 集成      | 无    | 无             | 无    | 自有闭源模型 | **LLM Gateway 可插拔**                |
| 支持模型     | N/A   | N/A            | N/A   | 闭源         | **OpenAI / DeepSeek / Ollama / 智谱** |
| 提示词模板   | N/A   | N/A            | N/A   | 无           | **8 套预置安全分析模板**              |
| 事件自动摘要 | ❌     | ❌              | ❌     | 部分         | **✅**                                 |
| 智能去误报   | ❌     | ❌              | ❌     | 部分         | **✅**                                 |
| 自然语言搜索 | ❌     | ❌              | ❌     | 无           | **✅ 支持中文**                        |
| 本地化部署   | N/A   | N/A            | N/A   | N/A          | **✅ Ollama 离线运行**                 |

### 功能一体化

| 能力         | Wazuh | Security Onion | Falco |    **CortexLens**     |
| ------------ | :---: | :------------: | :---: | :-------------------: |
| 日志采集     |   ✅   |       ✅        |   ❌   |         **✅**         |
| 资产自动发现 | 基础  |      间接      |   ❌   |   **✅ eBPF + 指纹**   |
| SIEM         |   ✅   |       ✅        |   ❌   |         **✅**         |
| 运行时安全   | 有限  |      有限      |   ✅   |         **✅**         |
| AI 智能分析  |   ❌   |       ❌        |   ❌   |   **✅ LLM Gateway**   |
| SOAR         | 基础  |      间接      |   ❌   | **✅ Temporal 工作流** |

---

## 🚀 快速开始

### 前置要求

- Docker & Docker Compose v2+
- 4GB 可用内存
- （可选）Go 1.22+（用于源码构建）

### 一键部署（推荐）

```bash
# 克隆仓库
git clone https://github.com/cortexlens/core.git
cd core

# 复制配置文件
cp configs/agent.yaml.example configs/agent.yaml
cp configs/server.yaml.example configs/server.yaml

# 编辑配置（可选）
vim configs/server.yaml  # 配置 LLM API Key 等

# 一键启动全部服务
make dev-up

# 打开控制台
open http://localhost:8080
```

### 从源码构建
```bash
# 构建 Agent
make build-agent

# 构建 Server
make build-server

# 运行全部测试
make test
```

### 安装 Agent（已有 Server 时）
```bash
# 在目标服务器上
curl -sSL https://get.cortexlens.io | bash

# 或使用 Docker
docker run -d \
  --name cortexlens-agent \
  --pid=host \
  --network=host \
  --privileged \
  -v /:/host:ro \
  -v /sys/kernel/debug:/sys/kernel/debug \
  cortexlens/agent:latest
```

## 🏗 架构概览

┌─────────────────────────────────────────────────────┐
│               可视化层 | Grafana + React 控制台        │
├─────────────────────────────────────────────────────┤
│             AI 智能分析层 | LLM Gateway + 提示词工厂    │
├─────────────────────────────────────────────────────┤
│        核心检测引擎 | Sigma 引擎 + Falco 引擎 + ML      │
├─────────────────────────────────────────────────────┤
│           流处理引擎 | Go Stream Processor             │
├─────────────────────────────────────────────────────┤
│  数据采集 | Go Agent (日志 + 指标 + eBPF + 资产发现)     │
└─────────────────────────────────────────────────────┘

## Docker Compose 部署拓扑

```
┌──────────────────────────────────────────────────┐
│                 docker-compose.yml                │
│                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐    │
│  │  Agent   │  │  Server  │  │    Kafka     │    │
│  │ (host    │  │  :50051  │  │    :9092     │    │
│  │ network) │  │  :8080   │  │              │    │
│  └──────────┘  └────┬─────┘  └──────────────┘    │
│                     │                            │
│         ┌───────────┼───────────┐                │
│         │           │           │                │
│  ┌──────┴──────┐ ┌──┴──────┐ ┌──┴──────────┐    │
│  │ ClickHouse  │ │PostgreSQL│ │  Grafana    │    │
│  │   :8123     │ │  :5432  │ │   :3000     │    │
│  └─────────────┘ └─────────┘ └─────────────┘    │
│                                                  │
│  可选服务：                                        │
│  ┌──────────┐                                    │
│  │  Ollama  │  ← 本地大模型（可选，离线 AI 分析）    │
│  │  :11434  │                                    │
│  └──────────┘                                    │
│                                                  │
│  资源需求：2 核 4G 即可运行全部服务                  │
└──────────────────────────────────────────────────┘
```

## 数据流转

```
数据源 → Agent → Kafka → Stream Processor → Detection Engine
                                               │
                                     ┌─────────┴─────────┐
                                     │                   │
                                Alert Pipeline      Storage Writer
                                     │                   │
                               ┌─────┴─────┐     ┌──────┴──────┐
                            AI Analyzer  SOAR    ClickHouse  PostgreSQL
```

## 🛡 内置检测能力

### 攻击类型覆盖（200+ 规则）

| 攻击类型            | 检测原理                           | 示例场景         |
| :------------------ | :--------------------------------- | :--------------- |
| 🐚 **Webshell 上传** | Web 进程写入 .php/.jsp 到 Web 目录 | 文件上传漏洞利用 |
| 💉 **命令注入**      | Web 进程执行 /bin/sh / cmd.exe     | RCE 漏洞利用     |
| 🔑 **SSH 暴力破解**  | 短时间大量登录失败                 | 密码猜解攻击     |
| 🔄 **反弹 Shell**    | 异常出站连接 + bash -i 特征        | 获取反向控制权   |
| ⬆️ **本地提权**      | sudo 滥用 / SUID 文件创建          | 权限提升         |
| ↔️ **横向移动**      | SSH/RDP 内部连接异常               | 内网渗透         |
| ⛏️ **挖矿程序**      | CPU 异常 + 矿池域名连接            | 植入挖矿木马     |
| 📦 **容器逃逸**      | 挂载宿主机敏感目录                 | Docker 安全      |
| 📤 **数据外泄**      | 大流量出站 / 敏感文件读取          | 数据窃取         |
| 🎯 **C2 通信**       | 周期性出站连接 + Beacon 特征       | APT 远控         |

### AI 智能分析能力

| 模板编号 | 功能         | 触发场景               |
| :------- | :----------- | :--------------------- |
| T-001    | 安全事件摘要 | 告警聚合为 Incident 时 |
| T-002    | 攻击链推演   | Incident 包含多条告警  |
| T-003    | 威胁等级研判 | 新告警产生时           |
| T-004    | 处置建议生成 | 告警确认后             |
| T-005    | 自然语言查询 | 用户搜索时             |
| T-006    | 安全态势总结 | 每日/每周报告          |
| T-007    | 溯源辅助     | 安全事件调查           |
| T-008    | 漏洞风险评估 | 新漏洞公告时           |

---

## 📚 文档

| 文档                                               | 说明                           |
| :------------------------------------------------- | :----------------------------- |
| [架构设计文档](https://docs/architecture.md)       | 完整系统架构与模块设计         |
| [提示词模板工厂](https://docs/prompt-templates.md) | 8 套 AI 安全分析提示词详细说明 |
| [API 参考](https://docs/api.md)                    | REST / gRPC API 文档           |
| [部署手册](https://docs/deployment.md)             | 生产环境部署指南               |
| [Sigma 规则编写](https://docs/sigma-rules.md)      | 自定义检测规则编写指南         |
| [SOAR 剧本开发](https://docs/playbooks.md)         | 自动化响应剧本开发指南         |
| [贡献指南](https://contributing.md/)               | 如何参与贡献                   |

---

## 🤝 社区

### 加入我们

| 渠道                     | 地址                                                         |
| :----------------------- | :----------------------------------------------------------- |
| 💬 **Discord**            | [discord.gg/cortexlens](https://discord.gg/cortexlens)       |
| 💡 **GitHub Discussions** | [github.com/cortexlens/core/discussions](https://github.com/cortexlens/core/discussions) |
| 🐦 **Twitter / X**        | [@CortexLens](https://twitter.com/CortexLens)                |
| 🎥 **YouTube**            | [CortexLens 频道](https://youtube.com/@CortexLens)           |
| 📧 **邮件**               | dev@cortexlens.io                                            |

### 贡献方式

我们欢迎所有形式的贡献！

| 方式             | 说明                                                         |
| :--------------- | :----------------------------------------------------------- |
| 🐛 **提交 Bug**   | [GitHub Issues](https://github.com/cortexlens/core/issues)   |
| 💡 **功能建议**   | [GitHub Discussions](https://github.com/cortexlens/core/discussions) |
| 📝 **代码贡献**   | Fork + PR，参考 [贡献指南](https://contributing.md/)         |
| 📖 **文档改进**   | 直接 PR 到 `docs/` 目录                                      |
| 🎨 **Sigma 规则** | 提交到 `rules/community/` 目录                               |
| 🌍 **国际化**     | 帮助翻译文档和控制台                                         |
| 🛡 **安全研究**   | 发现漏洞请发邮件到 security@cortexlens.io                    |

---

## 🗺 路线图

### 第一阶段（v1.0）：内核采集 + 双引擎检测 + AI 原生分析

| 时间    | 里程碑                     |
| :------ | :------------------------- |
| 2026 Q3 | v0.1 Alpha — 单机版 MVP    |
| 2026 Q4 | v0.5 Beta — 社区公测版     |
| 2027 Q1 | **v1.0 正式版** — 开源发布 |
| 2027 Q2 | v1.5 — AI 增强版           |

**v1.0 交付能力：**

- ✅ eBPF 内核级采集 + 资产自动发现
- ✅ Sigma + Falco 双引擎威胁检测
- ✅ 8 套 AI 安全分析提示词模板
- ✅ 200+ 内置检测规则
- ✅ Grafana 态势大屏 + React 控制台
- ✅ JWT 认证 + RBAC 权限
- ✅ SOAR 自动化响应
- ✅ Docker Compose 一键部署

### 第二阶段（v2.0）：智能体矩阵 + 全栈扩展

| 时间    | 里程碑          |
| :------ | :-------------- |
| 2027 Q3 | v2.0 Alpha      |
| 2027 Q4 | **v2.0 企业版** |

**新增能力：** 8 大安全智能体、多租户、K8s Helm Chart、UEBA、漏洞管理、商业情报源

### 第三阶段（v3.0）：AI 原生安全生态

| 时间    | 里程碑                |
| :------ | :-------------------- |
| 2028 Q4 | **v3.0 + Cloud SaaS** |

**新增能力：** 插件市场、联邦学习、自我进化、预测性防御、MSSP 版

---

## 📊 项目状态

| 指标       | 状态                        |
| :--------- | :-------------------------- |
| 开发阶段   | 🟡 Alpha（积极开发中）       |
| 生产就绪   | 🔴 尚未（预计 2027 Q1 v1.0） |
| 测试覆盖率 | 🟡 目标 > 70%                |
| 安全性     | 🟡 内部安全审计中            |
| 社区       | 🟢 欢迎早期贡献者            |

---

## 📄 许可证

CortexLens 采用 [Apache License 2.0](https://license/) 开源许可证。

Copyright © 2026 CortexLens Contributors.

---

## ⭐ Star 历史

![Star History](https://api.star-history.com/svg?repos=cortexlens/core&type=Date)

---

<p align="center">
  <strong>CortexLens</strong> —— 让安全态势感知不再是大厂的专利。
</p>

<p align="center">
  <sub>Open · Lightweight · AI-Native</sub>
</p>

<p align="center">
  <sub>Made with ❤️ by the CortexLens Team</sub>
</p>
