# 120天 AI-Native 程序员手写训练计划

规则：每天做 2 个前端小任务、2 个后端小任务、1 个工程/Review任务。第一版尽量自己手写；跑起来；自己看错误5分钟；再让AI修；最后把坑写进 `memory.md`。

> 说明：以下为训练计划主表（2026-05-05 ～ 2026-09-01）。

## 任务总表

已按你提供的计划原样整理（建议后续按周拆分到 `plan/weeks/` 便于维护）。

| 日期 | 前端任务1 | 前端任务2 | 后端任务1 | 后端任务2 | 工程/Review |
|---|---|---|---|---|---|
| 2026-05-05 | JS对象：手写user对象、增删改字段、printUser函数 | JS函数：formatUser、isEmpty、cloneUser | Java类：User类、构造方法、getter/setter、printInfo | Java方法：isAdult、rename、updateAge | Git初始化训练仓库，首次commit，写README |
| 2026-05-06 | JS数组：map/filter/find/reduce处理users | JS数组排序：按age、name排序 | Java List<User>：遍历、查找、过滤 | Java Stream基础：filter/map/collect | 看git diff，写出每个改动原因 |
| 2026-05-07 | JS解构/展开：updateUser(user, patch) | TS接口：User、Partial<User>、Readonly<User> | Java DTO转换：User -> UserDTO | Java泛型：Result<T>、PageResult<T> | 每天任务必须开分支，练git branch/checkout |
| 2026-05-08 | Promise：模拟fetchUser成功/失败 | async/await：loadUser、loading、error | Java异常：BusinessException、try/catch | Result.fail统一错误返回 | 练git restore/reset，丢弃错误修改 |
| 2026-05-09 | JS模块化：user.js/userService.js/main.js | TS模块：导出User类型和API函数 | Java包结构：entity/service/controller | Java Controller调用Service | 写memory.md，记录今天不会的语法 |
| 2026-05-10 | 表单校验：name/age/email | 字符串处理：解析CSV一行，trim和空字段处理 | Java校验CreateUserRequest | Java字符串split解析CSV生成Tag对象 | 写AGENTS.md第一版：禁止直接改main、必须写测试 |
| 2026-05-11 | JS分页：paginate(list,page,pageSize) | safeJsonParse：错误JSON不崩 | Java分页：PageRequest/PageResult<T> | 模拟全局异常处理 | 写REVIEW.md第一版：文件范围、业务、测试、日志 |
| 2026-05-12 | 纯JS用户CRUD：create/update/delete/find/list | 纯JS内存数据id自增和重复name校验 | Java内存UserService CRUD | Java Map<Long,User>模拟数据库 | 写DEBUG.md，记录一次错误定位过程 |
| 2026-05-13 | 不看旧代码重写JS用户CRUD | 用TS重写User类型和CRUD签名 | 不看旧代码重写Java UserService | 补BusinessException和Result | AI只review不修改，列出10个问题 |

> 后续日期（2026-05-14 ～ 2026-09-01）任务内容较长，建议直接粘贴到此文件继续维护，
> 或拆分成 `plan/weeks/week01.md` ... `week17.md`。当前雏形已预留结构与模板。

## 每日固定记录模板

```md
## YYYY-MM-DD

### 今天手写
- 前端1：
- 前端2：
- 后端1：
- 后端2：
- 工程/Review：

### 今天跑通的命令
- 

### 今天遇到的错误
- 

### 今天真正理解的点
- 

### 今天要写入 memory.md 的坑
- 
```

## 合并前固定检查

```text
1. git status
2. git diff
3. 前端：npm test / npm run build
4. 后端：mvn test / mvn package
5. 检查是否改了不该改的文件
6. 检查是否有日志、异常、测试、回滚方案
7. 满意才合并，不满意直接丢弃分支
```
