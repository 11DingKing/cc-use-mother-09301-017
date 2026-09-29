# 分类评价抽检编排

本项目维护分类评价抽检编排的领域约定、角色边界与样例数据，供后端服务、接口和自动化验证统一使用。当前契约覆盖监管团队、抽检专家、被抽高校，并明确风险抽样、利益冲突、可复现随机、批次恢复等关键约束。

## 目录

- `domain/contract.json`：领域角色、状态、约束和样例。
- `src/domain_contract/`：契约读取与确定性校验。
- `tools/check_contract.py`：命令行摘要检查。
- `tests/`：契约完整性回归测试。

## 验证

测试命令：`python3 -m unittest discover -s tests -v`

编译命令：`python3 -m compileall -q src tools tests`

命令行检查：`python3 tools/check_contract.py domain/contract.json`
