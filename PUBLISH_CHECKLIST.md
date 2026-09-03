# 发布前检查清单

在 GitHub 新建空仓库后，只从当前 `github_public_release` 目录初始化和提交，不要从它的父目录执行 `git add .`。

## 可以提交

- 根目录的 3 个 HTML 页面（首页及两个工具）；
- `hard_maps/index.html` 与 `nightmare_maps/index.html` 两个地图图库入口页；
- `hard_maps/` 中独立绘制的 30 张 PNG；
- `nightmare_maps/` 中独立绘制的 13 张 PNG；
- `screenshots/` 中四个公开页面的预览图；
- `README.md`、`NOTICE.md`、`LICENSE` 和 `.gitignore`。

## 不应提交

- 游戏客户端、EXE、DLL；
- `.wpk`、`.idx`、`.gim`、`.scn` 等资源；
- 游戏直接提取的地图、图标、音频、模型或字体；
- 反编译结果、解密密钥、解包和资源恢复脚本；
- 抓包、进程读取、自动操作或客户端修改工具。

## 提交前命令

在当前目录执行：

```bash
git status --short
find . -type f -size +5M -print
```

预期没有大于 5 MB 的文件。检查 `git status`，确认不存在来源不明的二进制文件后再提交。

## 推荐仓库设置

- 仓库描述使用“非官方玩家攻略工具”，不要使用“官方”字样；
- 首次发布建议保持非商业；
- GitHub Pages 从默认分支根目录部署；
- 开启 Issue，便于玩家报告版本和地图错误；
- 游戏更新后，在 README 标明数据对应的版本或验证日期。
