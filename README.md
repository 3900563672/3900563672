# 👋 你好，我是 hh

我专注于 **Kubernetes AI 推理调度与仿真**：把调度策略写成可运行、可观测、可验证的代码。

## 🔭 主力项目

[hello-k8s-ai](https://github.com/3900563672/hello-k8s-ai) —— 基于 Kubernetes 的 AI 推理调度与仿真平台：

- 11 个 CRD + 7 个 Controller，把租户、模型、节点、策略建模为 Kubernetes 原生资源
- Simulator 离散事件引擎模拟 AI 推理负载（1x~20x 动态倍速）
- React Dashboard 单入口：配置、流量、数据回放、监控面板（Grafana 内嵌）、填写指南
- Prometheus / OpenTelemetry / Jaeger / PostgreSQL 全链路可观测
- Docker Desktop 一键部署，历史快照与指标持久化

## 📦 项目一览

| 项目 | 说明 | 技术栈 |
| --- | --- | --- |
| [hello-k8s-ai](https://github.com/3900563672/hello-k8s-ai) | Kubernetes AI 推理调度与仿真平台 | Go · Kubernetes · React · TypeScript |
| [AI-JSON-Repair-Tool](https://github.com/3900563672/AI-JSON-Repair-Tool) | 按配置规则实时修复/转换 JSON API 响应的代理服务 | Go · Gin |

## 🛠️ 技术栈

Kubernetes · Kubebuilder · controller-runtime · Go · React · TypeScript · PostgreSQL · Prometheus · OpenTelemetry · Jaeger · Grafana · Docker

## 🤖 AI 协作理念

我深度使用 AI 协作开发，并为此建立了可复用的工程化体系：

- **文档按读者分层**：人类 / 本地 Agent / 远程 AI 各自独立入口，互不串读
- **变更全部归档**：change-history 记录为什么改、怎么改、如何回滚
- **CI 强制同步**：改源码必须同步映射文档，文档漂移被机械门禁拦截

## 📫 联系

- 通过 [GitHub Issues](https://github.com/3900563672/hello-k8s-ai/issues) 交流项目问题
- 随时欢迎对 hello-k8s-ai 提出想法与建议
