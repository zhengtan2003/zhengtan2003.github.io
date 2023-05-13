---
title: "Nest can't resolve dependencies of the <provider> (?). Please make sure that the argument <unknown_token> at index [<index>] is available in the <module> context."
date: 2023-05-13 12:20:06
tags: 小bug真要命
---
## 错误信息
```shell
Nest can't resolve dependencies of the <provider> (?). Please make sure that the argument <unknown_token> at index [<index>] is available in the <module> context.

Potential solutions:
- Is <module> a valid NestJS module?
- If <unknown_token> is a provider, is it part of the current <module>?
- If <unknown_token> is exported from a separate @Module, is that module imported within <module>?
  @Module({
    imports: [ /* the Module containing <unknown_token> */ ]
  })
```
## 解决方法
主要是**Module A**引用了**Module B**的**Service**，但**Module B**并没有**exports**。
```
@Module({
    ...
    exports: [XxxService],
})
```
[官网解决方法](https://docs.nestjs.com/faq/common-errors)
