# 飞牛监控 fnMonitor

<p>
  <img alt="Version" src="https://img.shields.io/badge/version-2.19.0-blue">
  <img alt="fnOS" src="https://img.shields.io/badge/fnOS-x86%20%7C%20arm64-success">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-orange">
</p>

飞牛 fnOS 系统监控应用（FPK 原生应用）：实时监控 **CPU / 内存 / 磁盘 / 网络 / 温度 / 功耗 / GPU**，支持 Docker 容器管理、端口占用、硬盘 SMART、历史趋势与提醒阈值，深浅色 + 5 种主色。**流量统计模块**（整机 / 网卡 / 容器上下行流量、今日 / 本月累计、容器流量排行、CSV 导出）与**功耗统计模块**（实时瓦数 + kWh 耗电量 + 电费估算，无 RAPL 时自动回退 TDP 估算模型，CSV 导出）。纯 Python 标准库 + 单文件前端，**零第三方依赖、完全离线可用**，数据仅保存在本机。

- 当前版本：**v2.19.0**
- 作者：**Misite齊** · 贡献者：**[iqiuzixuan](https://github.com/iqiuzixuan)**（新界面、虚拟机、安全加固、回归测试）、**[ttkl9559-cell](https://github.com/ttkl9559-cell)**（SAS 硬盘 SMART、硬盘巡检与告警、iDRAC 带外监控）
- 适用平台：fnOS **x86 + arm64**（最低系统版本 0.9.0）
- 默认端口：**8777**（可改）
- 运行身份：**root**（需访问 sysfs 风扇转速读取、docker.sock、virsh（libvirt）、smartctl 与 /proc 跨用户进程信息）
                                      |
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

完整日志见 [Releases](https://github.com/MisiteQ/fnmonitor/releases)。

## 📄 许可证

[MIT License](LICENSE) © 2026 Misite齊 · 部分代码 © 2026 iqiuzixuan · 部分代码 © 2026 ttkl9559-cell
