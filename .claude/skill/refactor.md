# Refactoring Skill

进行代码重构时遵循以下原则：

## 重构原则

1. **小步进行** - 每次只做一个小改动，确保可编译/可运行
2. **先有测试** - 在重构前为关键行为编写或确认测试存在
3. **保持行为** - 重构不改变外部可见行为
4. **消除坏味道** - 长方法、大类、重复代码、过长参数列表等

## 常见重构手法

- Extract Method（提取方法）
- Extract Variable（提取变量）
- Rename（重命名）
- Move Method/Class（移动方法/类）
- Replace Conditional with Polymorphism（用多态替代条件）
- Introduce Parameter Object（引入参数对象）

## 输出要求

- 说明每次重构的目的和具体步骤
- 重构后的代码应保持或提升可读性
- 如有破坏性变更需明确标注
