---
aliases: [Declaration]
tags: [cpp, programming]
---
# Declaration

A declaration introduces a *name* to a  [[cppTranslation|translation]] unit. A name is the identifier which denotes an entity.

```C++
int f(int);
```

In contrast to a [[cppDefinition|definition]], a declaration provides only the name and argument types to the compiler. There can be any number of declarations.

A function declaration may contain argument names, purely to help the reader of the program. Unless the declaration is also the definition, the compiler will ignore the names.

>[!note]
>A function cannot be called unless it has been previously declared.

## References

[[@cppconBackBasicsStructure2020]]
