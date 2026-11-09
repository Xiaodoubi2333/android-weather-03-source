# android-weather-03-source v1.0

「从头搭建」的 coolweather 源码版：保留教材原始目录结构与命名，供对照学习用，不含任何额外改造。与 [`android-weather-02-textbook`](https://github.com/Xiaodoubi2333/android-weather-02-textbook) 的差别在于本仓库是最小可编译骨架，方便逐行比对新旧代码。

包名 `com.oldweatherapp.android`，`compileSdk 34 / minSdk 23`。

## 文件结构

```text
app/src/main/java/com/coolweather/android/
├── MainActivity.java      入口，仅加载 activity_main
└── db/
    ├── Province.java      省
    ├── City.java          市
    └── County.java        县
app/src/main/res/layout/
├── activity_main.xml
└── choose_area.xml
```

## 启动

1. Android Studio 打开工程并同步；
2. 运行 `app`，当前仅有布局，无网络请求与业务逻辑；
3. 如需可运行的完整版，改用 [`android-weather-05-navigation`](https://github.com/Xiaodoubi2333/android-weather-05-navigation)。

依赖：`appcompat 1.0.2`、`constraintlayout 1.1.3`、`litepal 1.3.2`、`okhttp 3.4.1`、`gson 2.7`、`glide 3.7.0`。

## 功能落点表

| # | 功能 | 状态 | 落点 |
|---|---|---|---|
| 1 | 原始目录结构（教材一致） | 完成 | `com/coolweather/android/` |
| 2 | 地区三表实体 | 完成 | `db/Province`、`db/City`、`db/County` |
| 3 | 主界面与地区选择布局 | 完成 | `res/layout/activity_main.xml`、`choose_area.xml` |
| 4 | 业务逻辑 | 未实现 | 刻意留空，作为对照基线 |
| 5 | 天气数据接入 | 未实现 | — |

## 版本记录

### v0.1 · 建库

- `chore: 初始化仓库（LICENSE / .gitignore）`：网页端建库。

### v1.0 · 源码入库

- `feat: 导入教材 coolweather 原始源码作为对照基线`：完整源码一次性推入。

## 已知限制

- 只有三次提交，没有分阶段演进记录。
- `applicationId` 与 [`android-weather-01-skeleton`](https://github.com/Xiaodoubi2333/android-weather-01-skeleton)、[`android-weather-02-textbook`](https://github.com/Xiaodoubi2333/android-weather-02-textbook) 相同，三者不可同时安装。
