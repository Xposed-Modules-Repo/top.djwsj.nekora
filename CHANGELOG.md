# 更新日志

## 1.0.1

### Nekora 1.0.1 · 包名更正重发

本次保持版本名 1.0.1 重新发行，安装包名更正为 `top.djwsj.nekora`，展示名称仍为 Nekora。

#### 主要功能

- 将安装包名末段由 `nakora` 更正为 `nekora`，资源、已安装版本读取和激活状态跟随正确包名。
- 桌面主页显示已安装宿主、发行仓库地址和交流入口，点击仓库地址可查看适配说明与下载。
- 宿主设置页和分享面板中的模块入口、分类设置、账号信息查看及用户 ID 复制；工具页保留缓存重建和日志导出，不显示关于信息。
- 视频广告、运营弹窗及视频／图文内容过滤，视频信息显示与媒体保存。
- 点赞、收藏等防误触控制，顶栏、底栏、侧边栏和系统手势条的显示设置。
- 已捕获私信的防撤回提示、消息推荐净化和私信一键已读；极速版另提供消息数据查看和字段复制。
- 评论背景、详细日期时间及多维过滤，本地自定义评论仅在本机显示，不会真正发布。
- 查找缓存重建、进度和耗时提示、崩溃日志导出，以及经过安装包校验的应用内更新。
- 签到、搜索辅助及分享推送等条件功能需要本地开关、有效任务和相应服务权限，结果以宿主与服务实际判定为准。

#### 适配范围

| 宿主 | 包名 | 适配参考版本 |
| --- | --- | --- |
| 快手极速版 | `com.kuaishou.nebula` | 14.7.20、14.7.30.11804、14.7.40.11821、14.8.20、14.8.40.11936 |
| 快手标准版 | `com.smile.gifmaker` | 14.9.20.50799 |

以上为适配参考范围，不代表每个版本的全部功能均已完整实测，也不保证其间的所有小版本兼容。功能可用性还受动态插件、账号状态和设备环境影响，未列出的版本不作兼容承诺。

##### 运行要求

- 本次重发包名为 `top.djwsj.nekora`；与旧 `top.djwsj`、此前同版本的 `top.djwsj.nakora` 是不同应用，不能直接覆盖安装，旧模块 App 的数据不会自动迁移。
- 新旧包可以保留，但请在框架中只启用其中一个，避免对同一宿主重复注入。
- 安装下限为 Android 8.0（API 26）；实际可用系统版本还受宿主与框架限制。
- 正式 APK 仅提供 `arm64-v8a`，需要兼容的 64 位 ARM 设备和宿主进程。
- 使用支持 libxposed API 102 的框架，例如 Vector 2.2，并启用对应宿主作用域；旧 LSPosed 1.9.2 不支持此入口。
- 标准版、极速版与模块 App 的配置分别保存，开关不会自动相互同步。

#### 使用的开源仓库

| 项目 | 用途 | 仓库 |
| --- | --- | --- |
| libxposed API | 模块运行接口 | [libxposed/api](https://github.com/libxposed/api) |
| DexKit | 宿主功能适配 | [LuckyPray/DexKit](https://github.com/LuckyPray/DexKit) |
| AndroidX / Jetpack Compose | 界面、主题与基础组件 | [androidx/androidx](https://github.com/androidx/androidx) |
| Kotlin Coroutines | 异步任务与界面调度 | [Kotlin/kotlinx.coroutines](https://github.com/Kotlin/kotlinx.coroutines) |
| OkHttp | 网络连接与下载 | [square/okhttp](https://github.com/square/okhttp) |
| StringFog | 字符串处理 | [MegatronKing/StringFog](https://github.com/MegatronKing/StringFog) |

感谢上述开源项目及贡献者；项目名称与仓库归各自维护者所有。
