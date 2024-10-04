---
aliases: [C++ Define Directive]
tags: [cpp, programming]
---
# C++ Define Directive

`#define` generates a macro, which effectively replaces the instance of an identifier with a user-specified token string.

The compiler will substitute the token string for every instance of the identifier, but only if the identifier does not appear in a comment/string. The identifier itself has to form its own separate token.

>[!note]
>It is not generally considered best practice to use `#define` over alternatives such as `const`.

## References
[[@microsoftDefineDirective]]