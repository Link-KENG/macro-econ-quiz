# 宏观经济学 · 九至十四章刷题

《西方经济学》（第二版）下册 下篇宏观经济学（第九—十四章）章节刷题站，已发布 GitHub Pages：

**https://link-keng.github.io/macro-econ-quiz/**

## 功能（与银行从业七套卷答题站同款配置）

- **章节练习**：6 章各 15 单选 + 8 判断（每题 1 分），即答即判、附答案解析，答题卡任意跳题，提前交卷未答计错
- **模考**：从六章题库随机抽 20 单选 + 10 判断组卷，整卷作答后统一判分，作答过程中不显示答案，进度自动存档可续答
- **历史记录**：localStorage 持久化，点击任意一条可逐题回顾，结果页错题栏可展开；「再做一次」一键重练
- 配套考点讲义：https://link-keng.github.io/macro-econ-notes/

## 结构

- `data/macro.json`：全部题库（138 题 = 单选 90 + 判断 48），含答案与解析
- `js/app.js`：单页应用（无框架，同银从答题站引擎）
- 题目来源：《西方经济学》（第二版）下册 第九—十四章考点讲义整理，仅供学习参考

## 更新流程

本地 git 仓库即本目录。改题后：

```bash
python ../scripts/build_data.py      # 由 ../qs/ch*.json 重新生成 data/macro.json（含校验）
node ../scripts/test_site_app.js     # 前端回归测试（stub DOM，node 直接跑）
git add -A && git commit -m "更新" && git push
```

Pages 约 1-2 分钟生效。
