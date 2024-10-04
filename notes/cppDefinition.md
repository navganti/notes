---
aliases: [Definition]
tags: [cpp, programming]
---
# Definition

A C++ definition is a [[cppDeclaration|declaration]] that defines the entity. The set of definitions is a subset of declarations.

 >[!example]
>```cpp
>int f(int x) {
>    std::cout << x << std::endl;
>
>    return x + 1;
>}
>```

A definition *must* contain everything the compiler needs to compile and execute the program, while in contrast a declaration just provides the name and argument types to the compiler.

Definitions must conform to the [[oneDefinitionRule|One Definition Rule]].

## References

[[@cppconBackBasicsStructure2020]]
