# Dawnsdew Lulu's Table v0.6.5-Bata 返回导航与升级

## 目标

- 修复手机系统返回键在 Android 13+ 及兼容分发路径下直接退出 Activity 的问题。
- 在保留现有页面层级返回逻辑的基础上，首页连续两次返回才显示退出确认。
- 版本保持为 `versionCode 12` / `versionName 0.6.5-Bata`，使用本副本独立的 release 签名；该 APK 不覆盖安装源 app。

## 行为

- 详情、编辑、特典详情、食材匹配等页面优先执行各自的上一页动作。
- 没有显式返回动作的非首页页面返回首页。
- 首页第一次返回显示短提示；两秒内再次返回显示“退出应用？”确认框。
- 确认框选择“继续使用”或取消不会退出，选择“退出”才结束 Activity。
- 使用单一返回分发入口连接旧版 `onBackPressed` 和 Android 13+ `OnBackInvoked`，并过滤同一次系统手势的重复分发。

## 升级兼容

- 包名、命名空间和 SharedPreferences 数据键保持与源 app 一致；本副本使用独立 release 证书。
- release APK 版本号保持与源 app 的 v0.6.5-Bata 对齐；debug APK 仅用于开发验证，不用于覆盖 release 包。

## 验收

- 返回状态机单元测试覆盖首次返回、窗口内二次返回、超时和时钟回拨。
- Debug/Release Lint、单元测试、构建、签名和 APK 元数据检查通过。
