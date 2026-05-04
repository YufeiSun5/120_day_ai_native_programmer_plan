# 120天 AI-Native 程序员手写训练计划

规则：每天做 2 个前端小任务、2 个后端小任务、1 个工程/Review任务。第一版尽量自己手写；跑起来；自己看错误5分钟；再让AI修；最后把坑写进 `memory.md`。

## 任务总表

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
| 2026-05-14 | React UserCard组件：props显示用户 | React Button组件：disabled/loading props | Spring Boot GET /api/hello | 定义Result返回结构 | 保存Postman/HTTP请求文件 |
| 2026-05-15 | React useState计数器：+1/-1/reset | React受控输入框：name输入实时显示 | GET /api/users/{id}，PathVariable | Service里findById，不存在抛异常 | 写API.md：路径、参数、返回 |
| 2026-05-16 | React UserList：列表、key、空状态 | React Empty组件：暂无数据展示 | GET /api/users返回List<UserDTO> | DTO转换不暴露Entity | 定义日志规范：info/warn/error |
| 2026-05-17 | React UserForm：name/age/email受控表单 | 前端validateUserForm返回errors对象 | POST /api/users，RequestBody | CreateUserRequest后端校验 | 定义错误码：0/400/401/403/404/500 |
| 2026-05-18 | useEffect调用GET /api/users | 封装loading/error/empty三态显示 | 后端Map模拟数据库：list/find/create | 初始化3个用户 | 写.env.example，不提交真实key |
| 2026-05-19 | 表单提交POST，成功刷新列表 | LoadingButton防重复提交 | DELETE /api/users/{id} | 删除不存在返回BusinessException | Review删除功能：误删风险、确认、回滚 |
| 2026-05-20 | 列表删除按钮：确认、删除、刷新 | ErrorMessage组件：显示/关闭错误 | PUT /api/users/{id} | UpdateUserRequest只允许改部分字段 | Review更新功能：是否覆盖不该覆盖字段 |
| 2026-05-21 | 编辑用户：表单回填、PUT提交 | 退出编辑和重置表单 | RestControllerAdvice全局异常 | 捕获BusinessException和Exception | Review异常处理：有没有吞异常 |
| 2026-05-22 | 前端搜索框：本地过滤name | 搜索清空按钮恢复全部 | GET /api/users?keyword= | keyword为空返回全部 | Review搜索：空keyword、特殊字符 |
| 2026-05-23 | 前端调用后端搜索接口 | 搜索loading和error状态 | 分页GET /api/users?page=&pageSize= | 非法page/pageSize处理 | Review分页：total/items是否一致 |
| 2026-05-24 | 前端分页组件：上一页/下一页 | 分页状态和搜索条件联动 | 后端搜索+分页组合 | 先过滤再分页 | Git合并演练：feature合并main |
| 2026-05-25 | 封装userApi.ts：list/create/update/delete | 页面不直接写fetch | 整理controller/service/dto/request/common | Controller不写业务 | 制造git冲突并解决 |
| 2026-05-26 | 拆组件：UserPage/UserTable/UserForm/UserSearch | 补全TS类型：Result/PageResult/UserDTO | UserMapper：Entity/DTO/Request转换 | 补全Java DTO/Request/Entity边界 | GitHub Actions：前端npm test/build |
| 2026-05-27 | 完整用户管理页：列表/新增/编辑/删除/搜索/分页 | 前端人工review：组件大小、状态、错误处理 | 完整用户CRUD五个接口 | 后端人工review：分层、DTO、异常 | CI失败演练：故意写坏测试再修复 |
| 2026-05-28 | 动态表格columns渲染 | 表格空值显示：null/undefined显示'-' | 建users表：id/name/age/email/created_at | MyBatis selectAll | SQL EXPLAIN：看一次简单查询计划 |
| 2026-05-29 | 日期格式化createdAt | 创建后局部刷新列表 | MyBatis selectById | MyBatis insert返回自增id | 给name加索引，比较查询差异 |
| 2026-05-30 | 更新后前端局部替换数组项 | 乐观删除：失败后恢复 | MyBatis update | MyBatis deleteById | 慢SQL Review：检查有没有全表扫描 |
| 2026-05-31 | 后端错误码映射中文提示 | 表格checkbox：单选/全选/已选数量 | name唯一约束，捕获重复异常 | 批量删除POST /batch-delete | 事务Review：哪些操作必须一起成功 |
| 2026-06-01 | 批量删除联调 | 操作日志页面：action/target/time | @Transactional：createUserAndLog | operation_log表，创建/删除写日志 | 数据备份：导出SQLite/MySQL数据 |
| 2026-06-02 | request封装：自动解析Result，失败抛错 | 接口失败重试按钮 | 统一code：0/400/404/500 | 关键操作日志：创建/更新/删除/异常 | 数据恢复：从备份恢复 |
| 2026-06-03 | 前端测试纯函数：format/paginate/validate | 表单校验测试：空name/非法email | JUnit测试Service：成功/失败/不存在 | Service测试：插入/查询/更新/删除 | 测试覆盖Review：哪些核心路径没测 |
| 2026-06-04 | 前端mock API：成功/失败/loading | 页面失败重试按钮 | 后端接口测试：GET/POST/PUT/DELETE | 日志带id和参数摘要 | 写PR模板：变更内容、测试方式、风险 |
| 2026-06-05 | CSV粘贴预览页面 | CSV错误行显示：行号/原因/原文 | POST /api/users/import-preview解析CSV | CSV行校验：字段数/name/age/email | CSV安全Review：大文件、乱码、空行、重复行 |
| 2026-06-06 | CSV确认导入按钮 | CSV导出按钮，处理blob下载 | POST /api/users/import正式导入 | GET /api/users/export返回CSV | 导入幂等性：同一CSV导入两次会怎样 |
| 2026-06-07 | 写CSV_FRONTEND_REVIEW.md | 修复CSV导出Excel乱码 | 写CSV_BACKEND_REVIEW.md | 导入事务、重复数据、操作日志复盘 | 阶段复盘：CRUD/CSV最常见10个错误 |
| 2026-06-08 | MQTT前端状态面板：connected/disconnected/messageCount | MQTT消息列表：topic/payload/time | Java或Node连接broker，订阅test/topic | 向test/topic发布JSON消息 | 本地启动Mosquitto或EMQX |
| 2026-06-09 | MQTT连接配置表单：host/port/topic | MQTT消息过滤：按topic关键字过滤 | MQTT重连逻辑：断线重连、日志记录 | MQTT消息入库：topic/payload/created_at | MQTT QoS：理解0/1/2区别，记录适用场景 |
| 2026-06-10 | MQTT实时曲线：最近20条数值 | MQTT告警列表：value超过阈值标红 | MQTT解析工业点位：tag/value/timestamp | 后端告警规则：threshold判断并写alarm表 | MQTT retained message：测试保留消息 |
| 2026-06-11 | MQTT连接状态组件封装 | 前端SSE接收实时消息 | 后端MQTT服务类：connect/subscribe/publish/disconnect | 后端SSE推送MQTT最新消息 | MQTT clean session：理解断线后消息行为 |
| 2026-06-12 | SSE断线重连提示 | SSE消息面板显示最新点位值 | 后端SSE客户端管理 | 多浏览器同时接收MQTT转发 | MQTT topic设计：为工业点位设计topic规范 |
| 2026-06-13 | MQTT告警确认按钮 | 告警列表按时间倒序 | 告警确认接口ack alarm | 重复告警抑制：同tag同规则短时间不重复 | MQTT重连Review：断网、broker重启、认证失败 |
| 2026-06-14 | MQTT仪表盘小综合 | 写MQTT_FRONTEND_REVIEW.md | MQTT后端小综合：订阅/入库/告警/SSE | 写MQTT_BACKEND_REVIEW.md | SSE vs WebSocket vs MQTT对比表 |
| 2026-06-15 | 倒排索引前端：搜索框+结果列表 | 前端高亮搜索关键词 | 手写Java倒排索引Map<String,Set<Long>> | 分词：按空格/符号切词，小写化 | 倒排索引概念图：term -> docIds |
| 2026-06-16 | 搜索结果显示score | 搜索空状态/无结果状态 | 计算简单score：命中词数量 | 支持AND搜索：所有词都命中 | 分词Review：中文、英文、下划线、变量名怎么切 |
| 2026-06-17 | 搜索历史记录组件 | 搜索建议下拉框 | 支持OR搜索：任意词命中 | 词频统计：term -> count | AND/OR搜索写10组样例 |
| 2026-06-18 | 搜索分页 | 搜索过滤：按类型/日期 | 搜索结果分页 | 索引文档结构：id/title/content/type | 搜索分页Review：排序稳定性 |
| 2026-06-19 | 搜索结果高亮多个关键词 | 前端搜索防抖debounce | 实现snippet摘要 | 新增/删除文档同步更新索引 | 高亮Review：XSS风险 |
| 2026-06-20 | 搜索页loading/error/empty | 日志检索页面：action/user/time/keyword | 索引重建接口/rebuild-index | 日志搜索接口：按action/user/time/keyword | SQLite FTS5调研：了解能做什么 |
| 2026-06-21 | KIO变量表格：变量名/类型/地址/描述/单位 | KIO变量搜索：变量名/地址/类型 | KioVariable Entity和表结构 | KIO搜索接口支持分页 | SEARCH_CHECKLIST.md：分词、排序、更新风险 |
| 2026-06-22 | KIO新增表单和校验 | KIO编辑流程：回填/保存 | POST /api/kio-variables | PUT /api/kio-variables/{id} | KIO字段规则写入AGENTS.md |
| 2026-06-23 | KIO删除确认 | KIO右键菜单：编辑/删除/复制变量名 | DELETE /api/kio-variables/{id} | 删除写操作日志 | KIO操作日志Review |
| 2026-06-24 | KIO CSV导入预览 | KIO CSV错误行表格 | KIO CSV解析：name/type/address/desc/unit | 返回validRows/errorRows | KIO CSV字段顺序和编码Review |
| 2026-06-25 | KIO CSV正式导入 | KIO CSV导出按钮 | 导入事务、重复变量处理 | 导出字段顺序固定、中文不乱码 | 导入幂等性Review |
| 2026-06-26 | KIO批量选择/批量删除/批量导出 | KIO页面最终build修复 | 批量删除接口POST /batch-delete | 后端mvn test/package修复 | AI只review KIO，不允许修改 |
| 2026-06-27 | Java虚拟线程：前端显示并发测试结果 | 前端压测结果表格：任务数/耗时/成功数 | 写1000个虚拟线程sleep测试 | 虚拟线程HTTP调用模拟并发请求 | 虚拟线程Review：适合IO，不适合CPU密集 |
| 2026-06-28 | 前端任务进度条：并发任务完成百分比 | 前端取消任务按钮UI | 传统线程池ThreadPoolExecutor参数练习 | CompletableFuture并行查两个数据源再合并 | 线程池Review：核心线程、队列、拒绝策略 |
| 2026-06-29 | 前端显示共享计数器变化 | 前端显示并发错误日志 | synchronized保护共享计数器 | ReentrantLock手写加锁和finally释放 | 制造竞态条件并修复 |
| 2026-06-30 | 前端定时刷新任务状态 | 前端手动触发后台任务按钮 | @Scheduled定时扫描过期数据 | 手动触发定时任务接口 | 定时任务Review：重复执行、失败重试 |
| 2026-07-01 | 前端缓存命中状态显示 | 前端刷新缓存按钮 | Redis缓存变量详情，设置TTL | 缓存失效：更新变量后删除缓存 | Redis缓存Review：脏数据风险 |
| 2026-07-02 | 前端重复导入提示 | 前端显示锁占用状态 | Redis分布式锁概念：防止重复导入 | 导入接口加幂等key | 幂等性Review：重复请求不会重复写入 |
| 2026-07-03 | 前端登录表单 | 前端保存token并自动带请求头 | JWT登录接口 | JWT校验Filter/Interceptor | AUTH_REVIEW.md：token、过期、401 |
| 2026-07-04 | 前端权限路由：未登录跳登录 | 不同角色显示不同按钮 | 后端角色：admin/user | 接口权限校验 | 权限Review：前端隐藏不等于后端安全 |
| 2026-07-05 | 文件上传组件 | 上传进度条 | 后端文件上传接口 | 保存文件元信息，限制大小和扩展名 | 文件安全Review：扩展名、路径穿越、大小限制 |
| 2026-07-06 | 文件列表和下载按钮 | 文件删除确认 | 文件下载接口 | 文件删除接口，元数据一致 | 中文文件名和断点失败处理Review |
| 2026-07-07 | 大表格虚拟列表 | 前端debounce/throttle | 后端分页优化 | 后端限流概念 | 1万条数据不卡，记录优化前后 |
| 2026-07-08 | WebSocket前端封装 | WebSocket断线重连 | 后端WebSocket推送 | WebSocket心跳 | WebSocket/SSE/MQTT最终对比Review |
| 2026-07-09 | React Query查询缓存 | Zustand全局状态保存当前用户 | Redis缓存用户详情 | 缓存失效策略 | 前端状态管理Review |
| 2026-07-10 | ErrorBoundary错误边界 | Playwright E2E：登录/列表/新增 | 后端集成测试 | 测试数据初始化 | CI里自动跑前后端测试 |
| 2026-07-11 | Docker前端构建镜像 | 前端nginx静态部署配置 | 后端Dockerfile | 后端环境变量配置 | 镜像能启动 |
| 2026-07-12 | docker-compose前端+后端+DB | docker-compose加入MQTT broker | 后端连接compose里的数据库 | 后端连接compose里的MQTT | 一条命令启动全套 |
| 2026-07-13 | GitHub Actions构建前端镜像 | GitHub Actions上传前端产物 | GitHub Actions构建后端镜像 | GitHub Actions打包jar | CI产物可用 |
| 2026-07-14 | 前端性能检查：bundle大小和首屏 | 前端页面错误总复盘 | k6/JMeter压测接口 | 后端慢接口优化 | 记录QPS和耗时 |
| 2026-07-15 | 发布说明CHANGELOG | 版本号和tag | 后端版本接口/version | 数据库迁移脚本说明 | 能回滚到旧版本 |
| 2026-07-16 | AI最终Review前端，只review不修改 | 人工采纳/拒绝AI建议 | AI最终Review后端，只review不修改 | 修复最高风险问题 | 所有测试通过 |
| 2026-07-17 | 整理FRONTEND_GUIDE.md：启动/目录/API/常见错误 | 整理前端交接清单 | 整理BACKEND_GUIDE.md：接口/数据库/日志/测试/打包 | 整理部署和运维文档 | 别人能按文档启动 |
| 2026-07-18 | 总复盘：我现在能独立做什么 | 列出前端还看不懂的10项 | 总复盘：后端还看不懂什么 | 制定下一阶段学习计划 | 更新AGENTS.md/memory.md/skills总模板 |
| 2026-07-19 | TypeScript泛型组件：Table<T> | TS工具类型Pick/Omit/Record练习 | Java Record类：UserDTO用record重写 | 枚举Enum：UserStatus/VariableType | 类型边界Review：DTO字段是否稳定 |
| 2026-07-20 | React Hook自定义：useLoading | React Hook自定义：useApiError | Java Optional练习：避免空指针 | Bean Validation入门：@NotBlank/@Min | 空值Review：前后端空值策略一致 |
| 2026-07-21 | 前端路由：用户页/日志页/变量页 | 前端Layout：侧边栏和内容区 | Spring拦截器Interceptor记录请求耗时 | AOP记录接口日志 | 日志Review：耗时、路径、用户、结果 |
| 2026-07-22 | 前端主题切换：浅色/深色 | CSS模块化或Tailwind基础布局 | 配置文件application.yml分环境 | Profile：dev/test/prod | 配置Review：敏感信息不进git |
| 2026-07-23 | 前端大表格列宽调整 | 列显示隐藏配置 | 后端导出字段配置 | 字段配置保存到数据库 | 配置化Review：默认值和兼容旧数据 |
| 2026-07-24 | 前端拖拽排序小练习 | 前端保存排序结果 | 后端排序字段sort_order | 批量更新排序接口 | 批量更新事务Review |
| 2026-07-25 | 前端导入进度条 | 前端导入结果统计卡片 | 后端异步导入任务表import_task | 导入任务状态查询接口 | 异步任务Review：失败、重试、进度 |
| 2026-07-26 | 前端轮询任务状态 | 前端停止轮询条件 | 后端虚拟线程执行导入任务 | 后端任务取消标记 | 虚拟线程任务Review：取消和异常 |
| 2026-07-27 | 前端显示后台任务列表 | 前端任务详情页 | 后端任务日志表 | 任务日志查询接口 | 任务可观测性Review |
| 2026-07-28 | 前端下载导入错误报告 | 前端错误报告预览 | 后端生成错误CSV报告 | 错误报告文件下载接口 | 错误报告Review：行号、原文、原因 |
| 2026-07-29 | 前端变量详情抽屉 | 前端复制变量路径按钮 | 后端变量详情接口 | 后端变量引用关系表 | 引用关系Review：删除变量前检查 |
| 2026-07-30 | 前端变量引用关系展示 | 前端引用跳转 | 后端查询变量被哪些画面/脚本引用 | 后端维护引用索引 | 引用索引Review：更新一致性 |
| 2026-07-31 | 前端标签Tag组件 | 前端按标签过滤变量 | 后端变量标签表 | 标签增删改查接口 | 多对多关系Review |
| 2026-08-01 | 前端批量打标签 | 前端标签管理页 | 后端批量打标签事务 | 后端标签唯一约束 | 批量标签Review |
| 2026-08-02 | 前端报警规则配置表单 | 前端报警规则列表 | 后端报警规则Entity | 后端规则CRUD | 规则Review：阈值、单位、启停状态 |
| 2026-08-03 | 前端报警实时提示Toast | 前端报警确认弹窗 | 后端报警状态流转：new/ack/closed | 后端报警确认接口 | 报警状态机Review |
| 2026-08-04 | 前端报警历史搜索 | 前端报警导出 | 后端报警历史分页搜索 | 后端报警导出CSV | 报警检索Review |
| 2026-08-05 | 前端趋势图数据适配 | 前端最近N分钟选择器 | 后端时序数据表设计 | 后端按时间范围查询趋势 | 时序数据Review：时间戳、乱序、缺失 |
| 2026-08-06 | 前端图表loading/error | 前端图表空数据状态 | 后端聚合查询：min/max/avg | 后端降采样接口 | 大数据量Review |
| 2026-08-07 | 前端设备树组件 | 前端树节点搜索 | 后端设备层级表 | 后端递归查询设备树 | 树结构Review：循环引用 |
| 2026-08-08 | 前端设备树拖拽移动 | 前端移动确认 | 后端移动节点接口 | 后端防止移动到子节点 | 树移动事务Review |
| 2026-08-09 | 前端权限按钮封装 | 前端无权限提示 | 后端权限注解或手写校验 | 后端操作级权限检查 | 权限Review：按钮和接口双重控制 |
| 2026-08-10 | 前端审计日志页面 | 前端审计详情弹窗 | 后端审计日志记录before/after | 后端审计查询接口 | 审计Review：谁、何时、改了什么 |
| 2026-08-11 | 前端设置页：系统参数 | 前端保存设置 | 后端系统参数表 | 后端参数读取缓存 | 配置缓存Review |
| 2026-08-12 | 前端国际化雏形：zh/en字典 | 前端错误码翻译 | 后端错误码枚举 | 后端不返回硬编码中文 | 国际化Review |
| 2026-08-13 | 前端键盘快捷键：Ctrl+S保存 | 前端快捷键冲突处理 | 后端无新增，补接口测试 | 后端无新增，补异常测试 | 可用性Review |
| 2026-08-14 | 前端撤销/重做小练习 | 前端编辑历史栈 | 后端版本表variable_version | 后端保存变更版本 | 版本Review：回滚风险 |
| 2026-08-15 | 前端版本对比diff展示 | 前端回滚按钮 | 后端版本详情接口 | 后端回滚到某版本 | 回滚Review：审计和权限 |
| 2026-08-16 | 前端导入模板下载按钮 | 前端模板说明页 | 后端下载CSV模板 | 后端模板字段从配置生成 | 模板Review：字段变化兼容 |
| 2026-08-17 | 前端数据字典页面 | 前端字典项增删改 | 后端数据字典表 | 后端字典缓存 | 字典Review：删除被引用项 |
| 2026-08-18 | 前端表单根据字典渲染select | 前端字典加载失败处理 | 后端字典接口 | 后端字典权限 | 字典联调Review |
| 2026-08-19 | 前端离线提示组件 | 前端请求失败队列雏形 | 后端健康检查/actuator | 后端就绪检查readiness | 健康检查Review |
| 2026-08-20 | 前端网络恢复后重试 | 前端本地草稿保存localStorage | 后端幂等请求ID | 后端防重复提交 | 离线/重试Review |
| 2026-08-21 | 前端最终重构：目录和命名整理 | 前端删除无用代码 | 后端最终重构：包结构和命名整理 | 后端删除无用代码 | 代码清理Review |
| 2026-08-22 | 前端最终测试：主要页面手工验收 | 前端最终文档截图说明 | 后端最终测试：接口回归 | 后端最终压测一次 | 发布前Checklist |
| 2026-08-23 | 最终项目演示脚本：前端操作路径 | 最终项目演示录屏准备 | 最终项目演示脚本：后端接口和日志 | 最终部署包整理 | 交付复盘：哪些能独立做、哪些还依赖AI |
| 2026-08-24 | 下一阶段前端计划：React Query/Zustand深入 | 下一阶段前端计划：组件库和可视化 | 下一阶段后端计划：Spring Security/Redis/MQ深入 | 下一阶段后端计划：性能和架构 | 更新个人AGENTS.md、memory.md、skills模板 |
| 2026-08-25 | 补漏日：选择最薄弱的前端任务重做 | 补漏日：选择最薄弱的React任务重做 | 补漏日：选择最薄弱的Java任务重做 | 补漏日：选择最薄弱的Spring任务重做 | 把补漏结果写进复盘 |
| 2026-08-26 | 模拟真实需求：新增一个小功能，自己拆任务 | 模拟真实需求：写前端验收标准 | 模拟真实需求：写后端验收标准 | 模拟真实需求：让AI执行一次 | 你只review、测试、决定合并 |
| 2026-08-27 | 最终考试：不问AI手写一个前端CRUD骨架 | 最终考试：不问AI手写一个CSV预览 | 最终考试：不问AI手写一个Spring CRUD骨架 | 最终考试：不问AI手写一个事务导入骨架 | AI评分但不修改，记录薄弱点 |
| 2026-08-28 | 总复盘：整理100条个人踩坑记录 | 总复盘：整理20条前端review规则 | 总复盘：整理20条后端review规则 | 总复盘：整理20条工程交付规则 | 形成长期学习路线 |
| 2026-08-29 | 加练：前端复杂表单联动 | 加练：表单字段依赖和重置 | 加练：后端复杂校验规则 | 加练：校验失败返回字段级错误 | 字段级错误Review：前端能定位到具体字段 |
| 2026-08-30 | 加练：前端导入大文件UI | 加练：分片上传UI雏形 | 加练：后端分片上传接口雏形 | 加练：文件合并和校验hash | 大文件Review：中断、重试、清理临时文件 |
| 2026-08-31 | 加练：前端Web Worker处理大CSV | 加练：主线程不卡顿提示 | 加练：后端异步批处理队列 | 加练：批处理失败重试 | 性能Review：前后端谁负责重计算 |
| 2026-09-01 | 最终封版：前端文档、截图、启动流程 | 最终封版：前端常见问题FAQ | 最终封版：后端文档、接口、数据库、部署 | 最终封版：后端常见问题FAQ | 最终封版Review：交付给别人能否独立启动 |

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
