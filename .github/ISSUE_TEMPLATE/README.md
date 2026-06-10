# GitHub Issue Forms 模板

更新时间：2026-06-09

本目录保存 QuantSwap 公开反馈入口的 GitHub Issue Forms 源模板。实际启用时，把本目录下除 `README.md` 外的 yml 文件复制到仓库根目录：

```text
.github/
  ISSUE_TEMPLATE/
    config.yml
    bug_report.yml
    update_install.yml
    license_login.yml
    trade_execution.yml
    feature_request.yml
```

## 反馈入口

客户端 `feedback_url` 建议指向模板选择页：

```json
"feedback_url": "https://github.com/SwapAlgoLab/QuantSwap/issues/new/choose"
```

当前模板按内测期主要反馈类型拆分：

| 文件 | 用途 |
| --- | --- |
| `bug_report.yml` | 功能异常、界面异常、普通 Bug。 |
| `update_install.yml` | 安装、启动、检查更新、下载更新、安装并重启。 |
| `license_login.yml` | 授权激活、登录、设备绑定、授权服务器连接。 |
| `trade_execution.yml` | Steam、Buff、SteamDT、代理、交易任务真实执行异常。 |
| `feature_request.yml` | 功能建议和体验反馈。 |

## 维护规则

- 所有模板必须提醒用户不要提交 Steam 密码、Steam Guard、Cookie、授权码、设备 ID、API Key、Token、代理密码或支付敏感信息。
- 优先让用户粘贴客户端“关于”页复制出的脱敏诊断信息，不要求手动填写底层机器标识。
- 交易类问题必须区分是否发生真实外部动作，例如已下单、已付款、已上架、已下架或未发生。
- 授权类问题不要要求完整邮箱、完整授权码或设备 ID。
- 更新类问题要收集当前版本、检测到的新版本、发布通道和失败阶段。
- 如果后续启用 GitHub Private Vulnerability Reporting，再把安全漏洞入口写入 `config.yml` 的 `contact_links`。

