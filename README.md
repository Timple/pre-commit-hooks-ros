# pre-commit-hooks-ros

ros-related hooks for pre-commit <https://pre-commit.com/>

## Usage

Write your `.pre-commit-config.yaml` as below.

```yaml
repos:
  - repo: https://github.com/tier4/pre-commit-hooks-ros
    rev: v0.2.0
    hooks:
      - id: prettier-package-xml
      - id: sort-package-xml
```
