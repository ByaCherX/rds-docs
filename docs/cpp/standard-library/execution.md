---
description: "Learn more about: &lt;execution&gt;"
title: "&lt;execution&gt;"
ms.date: "01/15/2021"
f1_keywords: ["<execution>", "execution/std::execution", "std::execution"]
helpviewer_keywords: ["execution header"]
---
# `<execution>`

Describes the execution policies for parallel algorithms.

## Syntax

```cpp
namespace std {
    template<class T> inline constexpr bool is_execution_policy_v = is_execution_policy<T>::value;
}
namespace std::execution {
    inline constexpr sequenced_policy seq { unspecified };
    inline constexpr parallel_policy par { unspecified };
    inline constexpr parallel_unsequenced_policy par_unseq { unspecified };
}
```

### Classes and Structs

|Name|Description|
|-|-|
|[`is_execution_policy` Struct](is-execution-policy-struct.md)|Detects execution policies to exclude certain function signatures from otherwise ambiguous overload resolution participation.|
|[`parallel_policy` Class](parallel-policy-class.md)|Used as a unique type to disambiguate parallel algorithm overloading. Indicates that a parallel algorithm’s execution may be parallelized.|
|[`parallel_unsequenced_policy` Class](parallel-unsequenced-policy-class.md)|Used as a unique type to disambiguate parallel algorithm overloading. Indicates that a parallel algorithm’s execution may be parallelized and vectorized.|
|[`sequenced_policy` Class](sequenced-policy-class.md)|Used as a unique type to disambiguate parallel algorithm overloading. Specifies that a parallel algorithm’s execution may not be parallelized.|

## Requirements

**Header:** \<execution>

**Namespace:** stdext

## See also

[Header files reference](cpp-standard-library-header-files.md)\
[Thread safety in the C++ standard library](thread-safety-in-the-cpp-standard-library.md)\
[C++ standard library reference](cpp-standard-library-reference.md)
