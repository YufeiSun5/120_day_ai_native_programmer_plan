# 120天 AI-Native 程序员手写训练计划（任务雏形）

这个仓库用于**保持手感**：每天坚持手写小任务，先自己跑通、定位错误，再借助 AI 修复并记录踩坑。

## 目录结构

- `plan/120_day_plan.md`：完整 120 天计划（含每日任务表、每日记录模板、合并前检查清单）
- `daily/`：每日记录，建议命名 `YYYY-MM-DD.md`
- `frontend/`：前端练习代码
- `backend/`：后端练习代码
- `review/`：Review、复盘、规范文档
- `notes/memory.md`：长期踩坑与经验沉淀

## 使用建议（每天）

1. 从 `plan/120_day_plan.md` 找到当天任务。
2. 在 `daily/YYYY-MM-DD.md` 按模板记录。
3. 第一版尽量手写并跑起来。
4. 自己看错误 5 分钟后再让 AI 协助修复。
5. 把当日关键坑写入 `notes/memory.md`。

## 快速开始

```bash
mkdir -p daily frontend backend review notes
cp templates/daily_template.md daily/$(date +%F).md
```
