# 更新日志

<script setup>
import ChangelogEntry from '../../../.vitepress/theme/components/ChangelogEntry.vue'
</script>

DW 网卡更新记录如下：

<ChangelogEntry version="3.0.22" date="2026-08-06" :type="['minor']">

- **新增** 支持 TX zero-copy 发送路径。
- **新增** 支持自定义虚拟地址和物理地址转换函数。

</ChangelogEntry>

<ChangelogEntry version="3.0.21" date="2026-06-03" :type="['minor']">

- **新增** ifethtool 支持 TSO / GSO 配置。
- **新增** ifethtool 支持 MTU 配置。
- **新增** ifethtool 支持 MAC 地址配置。

</ChangelogEntry>

<ChangelogEntry version="3.0.20" date="2026-03-26" :type="['minor']">

- **新增** DW 网卡支持 ifethtool 功能。

</ChangelogEntry>

<ChangelogEntry version="3.0.19" date="2026-01-29" :type="['minor', 'patch']">

- **新增** 支持 SM90D325 设备树版本。
- **新增** 支持 X2000、M300 设备树版本。
- **修复** 恢复 PHY 和 phylink 修改，修复修改 MTU 相关问题。

</ChangelogEntry>

<ChangelogEntry version="3.0.18" date="2025-12-18" :type="['patch']">

- **修复** stmmac 组播过滤配置问题。
- **修复** 灵矽 HS100 网口执行 `ifdown` / `ifup` 后无法恢复使用的问题。
- **修复** RK3562 TCP 发包速度低的问题。
- **修复** FMQL 单网口加载失败的问题。

</ChangelogEntry>

<ChangelogEntry version="3.0.17" date="2025-09-28" :type="['minor', 'patch']">

- **新增** 支持 netfirewall 1.0.0。
- **新增** 支持 RK3568 Schneider PLC 无设备树版本。
- **修复** 无设备树版本加载 `dw_mac` 时打印 `Bus platform was not initialized` 的问题。
- **修复** ioctl 设置 MAC 地址返回值错误的问题。

</ChangelogEntry>

<ChangelogEntry version="3.0.16" date="2025-09-11" :type="['minor', 'patch']">

- **新增** 支持通过 `dwmac_debug_enable` 控制网卡驱动加载期间的调试输出。
- **新增** 支持全志 T536 设备树版本。
- **新增** 支持 AIO、iTOP RK3568 无设备树版本。
- **修复** 修改 MTU 时 `tx_desc_helper` 空指针问题。
- **修复** DW IP 版本低于 4.0 时 DMA reset 可能阻塞的问题。

</ChangelogEntry>

<ChangelogEntry version="3.0.15 及更早" date="2025-08-27" :type="['minor', 'patch']">

- **新增** 支持 FMQL DW1 无设备树版本。
- **新增** 支持 RK3576、RK3562 设备树版本。
- **新增** 支持硬件时间戳。
- **新增** 支持龙芯 2K300 设备树版本。
- **新增** 支持龙芯 2K1500 无设备树版本。
- **新增** 新增 regulator 弱函数，支持 RK3588 EVB7 和创龙板卡设备树版本。
- **新增** 支持 LXKA200 HS100 设备树版本。
- **新增** 支持 stmmac poll recv。
- **新增** 支持龙芯 2K2000 设备树版本。
- **新增** DW 代码权限管理。
- **新增** 支持 bspls2k1000la dwmac。
- **新增** RX zero-copy pool 调整为 `4 * dma_size`。
- **新增** 平台私有数据新增强制软件校验和能力，修复 LS2K1000 DW IP 不支持硬件校验和的问题。
- **新增** 新增部分 clock 弱函数。
- **新增** 支持芯驰 D9 设备树版本。
- **新增** 支持中断聚合。
- **新增** 支持设备树和无设备树 BSP 共用同一个驱动库。
- **新增** 新增 `dw_version` Shell 命令。
- **新增** 新增设备树环境检查信息。
- **新增** 支持创龙 RK3568 无设备树版本。
- **新增** 支持驱动自带 DTS 文件构建与使用。
- **新增** 支持 Xspirit2 无设备树版本。
- **新增** 使用 `dw-id` 格式设置设备名称。
- **新增** 支持带设备树的 linux compat layer 版本。
- **新增** 新增 D9 DW5 quirks。
- **新增** 支持 Linux 6.4 DW 网卡驱动在 SylixOS 中运行。
- **修复** 随机 MAC 地址生成问题，并禁用 `DWMAC_LOONGSON` 链接错误。
- **修复** 修改 MTU 可能导致 `rx_helper` 空指针的问题。
- **修复** MAC reset GPIO 功能问题。
- **修复** RK3588 运行 2544 测试时打印 job message 丢失的问题。
- **修复** RK3568、RK3588 获取错误 GRF / PHP_GRF 的问题。
- **修复** 合并 2K2000 代码后龙芯 2K1000 无法使用的问题。
- **修复** 龙芯 2K2000 无法将网卡速率设置为 100Mbit/s 的问题。
- **修复** 运行 set_mac 应用导致 `SemaphoreBDelete` 错误的问题。
- **修复** stmmac 接收错误包时打印 `skb is null` 的问题。
- **修复** FMQL AG102 GMAC1 `phy-mode` 配置问题。
- **修复** FMQL AG102 无法接收组播包的问题。
- **修复** 运行 set_mtu 应用导致 `SemaphoreBDelete` 错误的问题。
- **修复** PHY down 时 pbuf 未释放的问题。
- **修复** `pclk` 为空时 probe 失败的问题。
- **修复** FMQL 无法工作在 10M / 100M 模式的问题。
- **更新** `stmmac_open` 增加到 drvfuncs init 指针。
- **更新** 调整 stmmac TX lock 类型。
- **更新** FMQL DTS 新增另一个网口支持。

</ChangelogEntry>
