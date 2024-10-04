---
aliases: [C++ Lambda Expressions]
tags: [cpp, programming]
---
# Lambda Expressions in C++

A lambda expression is a way to define an *anonymous* function at the location its invoked. This can also be used to pass it as an argument to a function; this is very useful for [[cppDefinition|defining]] custom sorting algorithms.

>[!example]
>```cpp
>std::vector<int> nums;
>...
>std::sort(nums.begin(), nums.end(),
>    // Lambda expression begins 
>    [](int a, int b) {
>        return (std::abs(a) < std::abs(b));
>    }
 >   // end of lambda expression
> );
>```

In the above, the custom sorting operation uses the absolute value of the variables, instead of the actual value.

![[corob-msftLambdaExpressions_001.png]]

>[!note]
The capture clause can be defined as `[]` (default), `[&]` (reference), or `[=]` (value). This indicates how to capture any outside variables referenced in the lambda body.

In some cases, lambda expressions should be declared outside of the function. For example, in a `set` or `priority_queue`.

>[!example]
>```cpp
>std::unordered_map<int, int> counts;
>
>...
>
>auto comp = [](int a, int b) {
>    return numCounts[a] < numCounts[b];
>};
>
>std::priority_queue<int, std::vector<int>, decltype(comp)> q(comp);
>
>for (const auto &count : counts) {
>    q.push(count.second);
>}


## References

[[@microsoftLambdaExpressions]]
