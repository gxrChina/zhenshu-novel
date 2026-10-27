# 枕书（ZhenShu）

内部测试版的发布与更新通道。应用包名 `cn.zhenshu.app`，基于开源项目 [legado](https://github.com/gedoor/legado)（GPL-3.0）定制。

## 下载

进入 [Releases](../../releases/latest) 下载最新测试版 APK。每个 Release 的资产文件名固定为：

```
zhenshu_<tag>.apk
```

例如 tag 为 `v1.0.0-beta.61` 时，资产名为 `zhenshu_v1.0.0-beta.61.apk`。

## 应用内自动更新

应用启动约 3 秒后会在后台检查本仓库的最新 Release：

1. 请求 `https://github.com/gxrChina/zhenshu-novel/releases/latest`，跟随 302 取出 tag；
2. tag 与已知版本不同时弹出更新提示，展示 tag 作为版本标识；
3. 点「更新」直接下载 `zhenshu_<tag>.apk` 并拉起系统安装；
4. 点「手动更新」跳到本仓库 Releases 页面；
5. 同一 tag 只会提示一次；点「不再提示」会关闭自动检查，可在「我的 → 其它设置 → 检查更新」重新打开。

## 版本线约定

- 正式版本：`vX.Y.Z`（对应 APK 的 versionName / versionCode 同步提升）
- 内部测试版：`vX.Y.Z-beta.N`（versionName 与 versionCode 保持不变，仅 tag 递进）
- 每次发版必须满足：tag 与资产名一致、资产为已签名的 release APK

## 安装说明

- 覆盖安装需与已安装版本签名一致（本通道内所有 APK 使用同一签名）；
- 若提示「应用未安装」，先卸载旧版再安装（会清空本地书与阅读进度，建议先备份）。

## 致谢与许可

本项目基于 [legado](https://github.com/gedoor/legado) 定制，遵循 GPL-3.0。感谢 legado 作者与贡献者。
