# YAML 基本概念和用法

## 特性

- 大小写敏感
- 使用缩进表示层级关系
- 使用空格，不实用 tab
- 缩进多少不重要，重要的是对齐

## YAML 支持的数据结构

- 对象
- 数组
- 纯量

## 基本用法

```yaml
name: Cat &leo # 变量申明
animal: # 对象
  pets:
    - # 数组
      - *leo # 变量引用
      - Dog
      - Goldfish
str: > # > 表示折叠 | 表示保留换行符「-去掉末尾换行符，+保留末尾换行符」
  Hello
  World
rawStr: "Hello World" # 有空格和特殊字符的时候需要用引号，但引号会对特殊字符进行转义，双引号不会
number: 12.30
time: 2020-07-12T2020-07-12 22:09:01 # ISO 8601 时间格式
date: 2020-07-12
nullSym: ~
bool: true
```
