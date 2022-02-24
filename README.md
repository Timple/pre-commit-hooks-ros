# pre-commit-hooks-ros

[ROS]-related hooks for [pre-commit]

## Usage

Write your `.pre-commit-config.yaml` as below.

```yaml
repos:
  - repo: https://github.com/tier4/pre-commit-hooks-ros
    rev: v0.4.0
    hooks:
      - id: prettier-xacro
      - id: prettier-launch-xml
      - id: prettier-package-xml
      - id: sort-package-xml
      - id: ros-include-guard
```

## Hooks available

### prettier-xacro

Apply [Prettier] with [plugin-xml] to [xacro].

### prettier-launch-xml

Apply [Prettier] with [plugin-xml] to [launch.xml].

### prettier-package-xml

Apply [Prettier] with [plugin-xml] to [package.xml].

### sort-package-xml

Sort the dependent packages in [package.xml].
If you want to exclude a tag from sorting, add `<! -- no format -->` at the beginning of the line.

```xml
<!-- no format --> <depend>rclcpp</depend>
```

### ros-include-guard

Fix the macro name of include guards.

<!-- Links -->

[ros]: https://ros.org/
[pre-commit]: https://github.com/pre-commit/pre-commit
[prettier]: https://prettier.io/
[plugin-xml]: https://github.com/prettier/plugin-xml/
[xacro]: http://wiki.ros.org/xacro
[launch.xml]: https://design.ros2.org/articles/roslaunch_xml.html
[package.xml]: https://www.ros.org/reps/rep-0149.html
