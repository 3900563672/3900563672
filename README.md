<div align="center">
  <p>
    <img src="https://readme-typing-svg.demolab.com/?lines=Hi%2C+I%27m+hh+%F0%9F%91%8B;Building+Kubernetes+%26+AI+Infrastructure&font=Fira+Code&weight=600&size=26&duration=2200&pause=500&color=24292F&center=true&vCenter=true&width=480&height=40" alt="Typing SVG" />
  </p>
  <sub>Kubernetes · Go · AI 推理调度与仿真 · AI×Human Collaboration · Cloud Native &amp; Observability</sub>
</div>

---

## 关于我

专注 **Kubernetes 控制面工程**：把调度策略写成可运行、可观测、可验证的系统。完整实现过从 CRD 设计、Controller 开发、模拟器引擎到可观测性与前端闭环的端到端项目，并沉淀了一套可复用的工程方法。

同时，我也在系统性地研究 **AI 与人类在高复杂度工程中的协作**：不是把 AI 当代码生成器，而是当协作者——研究如何让它可交接、可追溯、可验证，并把实践沉淀为可复用的方法。

**核心能力**
- **控制面开发**：Kubebuilder / controller-runtime，11 个 CRD、7 个 Controller 的完整设计与实现
- **系统仿真**：离散事件引擎模拟 AI 推理负载，1x~20x 动态倍速，时间段切面（起点/终点全局状态 + 区间指标与 Trace）
- **可观测性**：Prometheus / OpenTelemetry / Jaeger / Grafana 全链路，告警规则实测验证，历史数据 PVC 持久化
- **故障排查**：从偶发环境故障到上游缺陷定位的完整方法论——探针复现、健康对照、源码指纹、官方互动，全证据链沉淀为可复现研究仓库
- **工程治理**：CI 全链路门禁、文档按读者分层、变更全归档，让项目可交接、可长期维护

---

## 📊 GitHub Overview

<div align="center">
  <a href="https://github.com/3900563672">
    <img height="140" src="https://github-readme-stats.vercel.app/api?username=3900563672&show_icons=true&hide_border=true&border_radius=8&bg_color=ffffff&title_color=24292f&text_color=57606a&icon_color=0969DA&include_all_commits=true" alt="GitHub stats" />
  </a>
  <a href="https://github.com/3900563672">
    <img height="140" src="https://github-readme-stats.vercel.app/api/top-langs/?username=3900563672&layout=compact&hide_border=true&border_radius=8&bg_color=ffffff&title_color=24292f&text_color=57606a&langs_count=6" alt="Top languages" />
  </a>
</div>

---

## 🔭 开源项目

### [hello-k8s-ai](https://github.com/3900563672/hello-k8s-ai)

基于 Kubernetes 的 **AI 推理调度与仿真平台**：用 CRD 把租户、模型、节点、策略建模为原生资源，Controller 收敛配置，Simulator 模拟推理负载，Dashboard 单入口可视化。

[![CI](https://github.com/3900563672/hello-k8s-ai/actions/workflows/test.yml/badge.svg)](https://github.com/3900563672/hello-k8s-ai/actions/workflows/test.yml)
[![Lint](https://github.com/3900563672/hello-k8s-ai/actions/workflows/lint.yml/badge.svg)](https://github.com/3900563672/hello-k8s-ai/actions/workflows/lint.yml)
[![Docs](https://github.com/3900563672/hello-k8s-ai/actions/workflows/docs.yml/badge.svg)](https://github.com/3900563672/hello-k8s-ai/actions/workflows/docs.yml)
[![License](https://img.shields.io/github/license/3900563672/hello-k8s-ai)](https://github.com/3900563672/hello-k8s-ai/blob/main/LICENSE)

| 维度 | 内容 |
| --- | --- |
| 控制面 | 11 个 CRD + 7 个 Controller（租户 / 模型 / 节点 / 流量 / 时钟 / 编排 / 性能） |
| 仿真 | Simulator 离散事件引擎，1x~20x 倍速，时间段切面与确定性回放基础 |
| 可观测 | Prometheus + OTel + Jaeger + Grafana，告警规则实测触发验证 |
| 数据 | PostgreSQL 持久化历史快照，Prometheus / Jaeger PVC 不丢历史 |
| 部署 | Docker Desktop 一键部署，CI 含单测 / lint / 文档门禁 / E2E |
| 文档 | 人类 / 本地 Agent / 远程 AI 三层独立维护，变更全归档 |

### [wsl-loopback-stall](https://github.com/3900563672/wsl-loopback-stall)

WSL2（Consomme 网络模式）下 **IPv4 回环 + 临时端口 churn 引发的连接停滞**：从"偶发环境问题"到"上游缺陷区间定位"的完整研究链——确定性复现、剂量响应机制、DLL 指纹锚定、源码级修复确认，并已与上游官方互动（issue #41286 跟进评论 + 正式报告 #41383）。

[![Docs](https://github.com/3900563672/wsl-loopback-stall/actions/workflows/docs.yml/badge.svg)](https://github.com/3900563672/wsl-loopback-stall/actions/workflows/docs.yml)
[![License](https://img.shields.io/github/license/3900563672/wsl-loopback-stall)](https://github.com/3900563672/wsl-loopback-stall/blob/main/LICENSE)

| 维度 | 内容 |
| --- | --- |
| 复现 | 探针驱动确定性复现（2.7.8.0 / 2.9.4.0 复现，固定端口免疫，Docker 排除） |
| 机制 | 剂量响应定量模型（约 10.4ms/bind 固定开销、96 bind/s 恒定吞吐） |
| 证据 | DLL 字符串指纹全命中（tcp 27/27、udp 7/7）+ 源码级修复确认（2.9.5+） |
| 官方 | 上游 issue #41286 跟进评论 + 正式报告 #41383（官方日志包已交付、机器人放行） |
| 文档 | 39 篇编号文档全链路归档，markdownlint / 链接检查门禁 |

### [AI-JSON-Repair-Tool](https://github.com/3900563672/AI-JSON-Repair-Tool)

按配置规则实时修复 / 转换 JSON API 响应的代理服务（Go + Gin）。

---

## 🔬 AI × Human 协作研究

我在研究一个具体问题：**AI 如何参与高复杂度、长周期的工程而不失控**。不是把 AI 当代码生成器，而是当协作者——研究它的交接、追溯、验证与边界。

**研究问题**
- 如何让 AI 的产出可交接、可追溯、可回滚？
- 单人 + AI 协作能达到什么工程规范上限？
- AI 参与上游开源时，披露与信任边界在哪？

**我的实践**
- **文档按读者分层**：人类 / 本地 Agent / 远程 AI 独立入口，互不串读
- **变更全归档**：change-history 记录"为什么改、怎么改、怎么回滚"
- **CI 强制同步**：源码变更必须同步文档，漂移被门禁拦截
- **提示词协议化**：任务五要素、默认假设、交接模板，任何 AI 接手即对齐

**实验场**
- hello-k8s-ai：单人 + AI 达到团队级工程规范的全流程实验
- Kueue 上游：AI 辅助的真实开源贡献，全程透明 AI 披露
- WSL 上游缺陷研究：AI 辅助从复现到源码级确认的完整证据链

这套体系欢迎讨论：AI 协作的边界、规范、未来形态，我都感兴趣。

---

## 🤝 开源协作

- 项目欢迎 **Issue / PR / 讨论**：新想法、bug 报告、设计建议都欢迎
- 贡献指南：[CONTRIBUTING.md](https://github.com/3900563672/hello-k8s-ai/blob/main/CONTRIBUTING.md)
- 从 [good first issue](https://github.com/3900563672/hello-k8s-ai/labels/good%20first%20issue) 开始
- 安全漏洞：通过 [SECURITY.md](https://github.com/3900563672/hello-k8s-ai/blob/main/SECURITY.md) 私密报告

## 🛠️ Tech Stack

<table align="center">
  <tbody>
    <tr>
      <td width="150"><sub><b>⚙️ Backend</b></sub></td>
      <td align="left">
        <a href="https://go.dev"><img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" height="16" alt="Go" /></a>
        <a href="https://gin-gonic.com"><img src="https://img.shields.io/badge/Gin-008ECF?style=flat-square&logo=gin&logoColor=white" height="16" alt="Gin" /></a>
        <a href="https://kubebuilder.io"><img src="https://img.shields.io/badge/Kubebuilder-326CE5?style=flat-square&logo=kubernetes&logoColor=white" height="16" alt="Kubebuilder" /></a>
        <a href="https://github.com/kubernetes-sigs/controller-runtime"><img src="https://img.shields.io/badge/controller--runtime-24292F?style=flat-square" height="16" alt="controller-runtime" /></a>
      </td>
    </tr>
    <tr>
      <td width="150"><sub><b>☁️ Cloud &amp; DevOps</b></sub></td>
      <td>
        <a href="https://kubernetes.io"><img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" height="16" alt="Kubernetes" /></a>
        <a href="https://www.docker.com"><img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" height="16" alt="Docker" /></a>
        <a href="https://helm.sh"><img src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white" height="16" alt="Helm" /></a>
        <a href="https://github.com/features/actions"><img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" height="16" alt="GitHub Actions" /></a>
      </td>
    </tr>
    <tr>
      <td width="150"><sub><b>📈 Observability</b></sub></td>
      <td>
        <a href="https://prometheus.io"><img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" height="16" alt="Prometheus" /></a>
        <a href="https://grafana.com"><img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" height="16" alt="Grafana" /></a>
        <a href="https://www.jaegertracing.io"><img src="https://img.shields.io/badge/Jaeger-66CFE3?style=flat-square&logo=jaeger&logoColor=white" height="16" alt="Jaeger" /></a>
        <a href="https://opentelemetry.io"><img src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white" height="16" alt="OpenTelemetry" /></a>
        <a href="https://www.postgresql.org"><img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" height="16" alt="PostgreSQL" /></a>
      </td>
    </tr>
    <tr>
      <td width="150"><sub><b>🎨 Frontend</b></sub></td>
      <td>
        <a href="https://react.dev"><img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" height="16" alt="React" /></a>
        <a href="https://www.typescriptlang.org"><img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" height="16" alt="TypeScript" /></a>
        <a href="https://vite.dev"><img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" height="16" alt="Vite" /></a>
      </td>
    </tr>
    <tr>
      <td width="150"><sub><b>🧰 Tools &amp; AI</b></sub></td>
      <td>
        <a href="https://git-scm.com"><img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" height="16" alt="Git" /></a>
        <a href="https://www.linux.org"><img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=111111" height="16" alt="Linux" /></a>
        <a href="https://www.python.org"><img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" height="16" alt="Python" /></a>
        <a href="https://openai.com/codex"><img src="https://img.shields.io/badge/Codex-000000?style=flat-square" height="16" alt="Codex" /></a>
        <a href="https://claude.com"><img src="https://img.shields.io/badge/Claude-D17A5F?style=flat-square&logo=claude&logoColor=white" height="16" alt="Claude" /></a>
      </td>
    </tr>
  </tbody>
</table>

---

<div align="center"><sub>Thanks for visiting my profile! · 欢迎交流与协作</sub></div>