---
aliases: [C++ Main Function & Command Line Arguments]
tags: [cpp, programming]
---
# C++ Main Function & Command Line Arguments

Command line arguments can be passed to a C++ program by specifying your main function as follows:

>[!example]
>```cpp
> /// First option
> int main(int argc, char** argv) {
> ...
> }
 >
 > /// Second option
> int main(int argc, char* argv[]) {
> ...
> }

`argc` indicates the number of strings pointed to by `argv`. This is usually 1+ the number of arguments (since calling the program itself will require the executable name).

`argv` is a double pointer, and is required as explained [here](https://stackoverflow.com/questions/7631282/pointer-to-pointer-with-argv/7638048). It is a pointer to a `char*`, or a string. We can access the different arguments with `argv[n]` - this is equivalent to `*(argv + n)`, expressed in a more convenient manner. Each increment of `argv` will offset it by `sizeof(char*)`, corresponding to the size of each respective string in bytes.

## References

[[@microsoftMainFunctionCommandline]]
