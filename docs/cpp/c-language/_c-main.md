---
description: "C Language Main Reference"
title: "C Language Main Reference"
ms.custom: "index-page"
ms.date: "06/06/2021"
f1_keywords: ["c"]
helpviewer_keywords: ["Visual C", "C, language reference", "Visual C, language reference", "language reference, C"]
ms.assetid: 3a306c30-8dd2-435b-bd1c-c143b02c0872
---

<h1 style="text-align: center">C language Reference</h1>

The *C Language Reference* describes the C programming language as implemented in Microsoft C. The book's organization is based on the ANSI C standard (sometimes referred to as C89) with additional material on the Microsoft extensions to the ANSI C standard.

## C language Reference Tree

### [Organization of the C Language Reference](../c-language/organization-of-the-c-language-reference.md)
---
* #### [Scope of this manual](scope-of-this-manual.md)
* #### [ANSI conformance](ansi-conformance.md)

### [Elements of C](../c-language/elements-of-c.md)
---
* #### [C_Tokens](../c-language/c-tokens.md)
  * [White space characters](../white-space-characters.md)
  * [Comments](../c-language/c-comments.md)
  * [Evaluation of tokens](evaluation-of-tokens.md)
* #### [C_Keywords](../c-language/c-keywords.md)
* #### [C_Identifiers](../c-language/c-identifiers.md)
  * [Trigraphs](../c-language/trigraphs.md)
* #### [C_Constants](../c-language/c-constants.md)
  * [Floating-point](../c-language/c-floating-point-constants.md)
  * [integer](../c-language/c-integer-constants.md)
  * [integer types](../c-language/integer-types.md)
  * [C and C++ integer limits](cpp-integer-limits.md)
  * [Character constants](../c-language/c-character-constants.md)
  * [Character types](character-types.md)
  * [Execution character set](execution-character-set.md)
  * [Escape sequences](escape-sequences.md)
  * [Octal and hexadecimal character specifications](octal-and-hexadecimal-character-specifications.md)
* #### [C_String literals](../c-language/c-string-literals.md)
  * [Storage of string literals](storage-of-string-literals.md)
  * [String literal concantenation](string-literal-concantenation.md)
  * [Maximum string length](maximum-string-length.md)
* #### [Punctuation and special characters](../c-language/punctuation-and-special-characters.md)

### [Program Structure](../c-language/program-structure.md)
---
* #### [Source files and source programs](../c-language/source-files-and-source-programs.md)
  * [Directives to the preprocessor](../c-language/directives-to-the-preprocessor.md)
  * [C pragmas](../c-language/c-pragmas.md)
  * [C declarations and definitions](../c-language/c-declarations-and-definitions.md)
  * [Blocks](../c-language/blocks.md)
  * [Example Program](../c-language/example-program.md)
* #### [The main function and program execution](../c-language/main-function-and-program-execution.md)
  * [Argument description](argument-description.md)
  * [Parsing c command line arguments](parsing-c-command-line-arguments.md)
  * [Parsing command-line arguments](../c-language/parsing-c-command-line-arguments.md)
* #### [Lifetime, scope, visibility, and linkage](../c-language/lifetime-scope-visibility-and-linkage.md)
  * [Lifetime](../c-language/lifetime.md)
  * [Scope and visibility](../c-language/scope-and-visibility.md)
  * [Linkage](../c-language/linkage.md)
  * [Summary of lifetime and visibility](summary-of-lifetime-and-visibility.md)
* #### [Name spaces](../c-language/name-spaces.md)
### [Declarations and Types](../c-language/declarations-and-types.md)
---
* #### [Overview of declarations](../c-language/overview-of-declarations.md)
* #### [Storage classes](../c-language/c-storage-classes.md)
   * [Storage-Class Specifiers for External-Level Declarations](../c-language/storage-class-specifiers-for-external-level-declarations.md)
   * [Storage-Class Specifiers for Internal-Level Declarations](../c-language/storage-class-specifiers-for-internal-level-declarations.md)
     * [register storage class specifier](register-storage-class-specifier.md)
     * [static storage class specifier](static-storage-class-specifier.md)
     * [auto storage class specifier](auto-storage-class-specifier.md)
     * [extern storage class specifier](extern-storage-class-specifier.md)
   * [Storage-Class Specifiers with Function Declarations](../c-language/storage-class-specifiers-with-function-declarations.md)
* #### [Type specifiers](../c-language/c-type-specifiers.md)
   * [Data type specifiers and equivalents](data-type-specifiers-and-equivalents.md)
* #### [Type qualifiers](../c-language/type-qualifiers.md)
* #### [Declarators and variable declarations](../c-language/declarators-and-variable-declarations.md)
   * [Simple variables](../c-language/simple-variable-declarations.md)
   * [Enumeration variables](../c-language/c-enumeration-declarations.md)
   * [Structures](../c-language/structure-declarations.md)
     * [C bit fields](c-bit-fields.md)
     * [storage and alignment of structures](storage-and-alignment-of-structures.md)
     * [storage and alignment of structures](storage-and-alignment-of-structures.md)
   * [Unions](../c-language/union-declarations.md)
     * [storage of unions](storage-of-unions.md)
   * [Arrays](../c-language/array-declarations.md)
     * [storage of arrays](storage-of-arrays.md)
   * [Pointers](../c-language/pointer-declarations.md)
     * [storage of addresses](storage-of-addresses.md)
     * [based pointers c](based-pointers-c.md)
   * [C abstract declarator](c-abstract-declarator.md)
* #### [Interpreting more complex declarators](../c-language/interpreting-more-complex-declarators.md)
* #### [Initialization](../c-language/initialization.md)
   * [scalar types](../c-language/initializing-scalar-types.md)
   * [aggregate types](../c-language/initializing-aggregate-types.md)
   * [strings](../c-language/initializing-strings.md)
* #### [Storage of basic types](../c-language/storage-of-basic-types.md)
   * [Type char](type-char.md)
   * [Type int](type-int.md)
   * [C sized integer types](c-sized-integer-types.md)
   * [Type float](type-float.md)
   * [Type double](type-double.md)
   * [Type long double](type-long-double.md)
* #### [Incomplete types](../c-language/incomplete-types.md)
* #### [Typedef declarations](../c-language/typedef-declarations.md)
* #### [C Extended storage-class attributes](../c-language/c-extended-storage-class-attributes.md)
   * [Thread local storage](thread-local-storage.md)
### [Expressions and Assignments](../c-language/expressions-and-assignments.md)
---
* #### [Operands and expressions](operands-and-expressions.md)
   * [C primary expressions](c-primary-expressions.md)
     * [constants in primary expressions](constants-in-primary-expressions.md)
     * [identifiers in primary expressions](identifiers-in-primary-expressions.md)
     * [string literals in primary expressions](string-literals-in-primary-expressions.md)
     * [expressions in parentheses](expressions-in-parentheses.md)
     * [generic selection (C11)](generic_selection.md)
   * [L-value and r-value expressions](../c-language/l-value-and-r-value-expressions.md)
   * [C constant expressions](c-constant-expressions.md)
   * [Expressions evaluation C](expression-evaluation-c.md)
     * [Side effects](../c-language/side-effects.md)
     * [C sequence points](c-sequence-points.md)
* #### [Operators](../c-language/c-operators.md)
   * [Precedence and order of evaluation](precedence-and-order-of-evaluation.md)
   * [Usual arithmetic conversions](usual-arithmetic-conversions.md)
   * [Postfix operators](postfix-operators.md)
     * [one dimensional arrays](One-dimensional-arrays.md)
     * [multidimensional arrays](multidimensional-arrays.md)
     * [function call C](function-call-c.md)
     * [structure and union members](structure-and-union-members.md)
     * [C postfix increment and decrement operators](c-postfix-increment-and-decrement-operators.md)
   * [C unary operators](c-unary-operators.md)
     * [prefix increment and decrement operators](prefix-increment-and-decrement-operators.md)
     * [indirection and address of operators](indirection-and-address-of-operators.md)
     * [unary arithmetic operators](unary-arithmetic-operators.md)
     * [sizeof operator C](sizeof-operator-c.md)
   * [Cast operators](cast-operators.md)
   * [C multiplicative operators](c-multiplicative-operators.md)
   * [C additive operators](c-additive-operators.md)
     * [addition (+)](addition-plus.md)
     * [subtraction (-)](subtraction-minus.md)
     * [using the additive operators](using-the-additive-operators.md)
     * [pointer arithmetic](pointer-arithmetic.md)
   * [Bitwise shift operators](bitwise-shift-operators.md)
   * [C relational and equality operators](c-relational-and-equality-operators.md)
   * [C bitwise operators](c-bitwise-operators.md)
   * [C logical operators](c-logical-operators.md)
   * [Conditional expression operator](conditional-expression-operator.md)
   * [C assignment operators](c-assignment-operators.md)
     * [Simple assignment C](simple-assignment-c.md)
     * [C compound assignment](c-compound-assignment.md)
   * [Sequential evaluation operator](sequential-evaluation-operator.md)
* #### [Type conversions](../c-language/type-conversions-c.md)
   * [Assignment Conversions](assignment-conversions.md)
     * [conversions from signed integral types](conversions-from-signed-integral-types.md)
     * [conversions from unsigned integral types](conversions-from-unsigned-integral-types.md)
     * [conversions from floating point types](conversions-from-floating-point-types.md)
     * [conversions to and from pointer types](conversions-to-and-from-pointer-types.md)
     * [conversions from other types](conversions-from-other-types.md)
   * [Type cast conversions](type-cast-conversions.md)
   * [Function-call conversions](function-call-conversions.md)
### [Statements](../c-language/statements-c.md)
---
* [Break statement](../c-language/break-statement-c.md)
* [Compound statement](../c-language/compound-statement-c.md)
* [Continue statement](../c-language/continue-statement-c.md)
* [Do-while statement](../c-language/do-while-statement-c.md)
* [Expression statement](../c-language/expression-statement-c.md)
* [For statement](../c-language/for-statement-c.md)
* [Goto and labeled statements](../c-language/goto-and-labeled-statements-c.md)
* [if statement](../c-language/if-statement-c.md)
* [Null statement](../c-language/null-statement-c.md)
* [Return statement](../c-language/return-statement-c.md)
* [Switch statement](../c-language/switch-statement-c.md)
* [Try-except statement](../c-language/try-except-statement-c.md)
* [Try-finally statement](../c-language/try-finally-statement-c.md)
* [While statement](../c-language/while-statement-c.md)
### [Functions](../c-language/functions-c.md)
---
* #### [Overview of functions](../c-language/overview-of-functions.md)
* #### [C function definitions](c-function-definitions.md)
  * [Function attributes](../c-language/function-attributes.md)
    * [inline functions](inline-functions.md)
    * [inline assembler C](inline-assembler-c.md)
    * [noreturn](noreturn.md)
  * [Storage class](../c-language/storage-class.md)
  * [Return type](../c-language/return-type.md)
  * [Parameters](../c-language/parameters.md)
* #### [Function calls](function-calls.md)
  * [Arguments](../c-language/arguments.md)
  * [Recursive functions](recursive-functions.md)
### [C Language Syntax Summary](../c-language/c-language-syntax-summary.md)
---
*  [Definitions and conventions](definitions-and-conventions.md)
*  [Lexical grammar](lexical-grammar.md)
*  [Phrase structure grammar](phrase-structure-grammar.md)
   * [Expressions](../c-language/summary-of-expressions.md)
   * [Declarations](../c-language/summary-of-declarations.md)
   * [Statements](../c-language/summary-of-statements.md)
   * [External Definitions](../c-language/external-definitions.md)
### [Implementation-Defined Behavior](../c-language/implementation-defined-behavior.md)
---
* #### [Environment](environment.md)
  * [Arguments to main](../c-language/arguments-to-main.md)
  * [Interactive Devices](../c-language/interactive-devices.md)
* #### [Behavior of identifiers](behavior-of-identifiers.md)
  * [Significant Characters Without External Linkage](../c-language/significant-characters-without-external-linkage.md)
  * [Significant Characters with External Linkage](../c-language/significant-characters-with-external-linkage.md)
  * [Uppercase and Lowercase](../c-language/uppercase-and-lowercase.md)
* #### [Characters](characters.md)
  * [The ASCII Character Set](../c-language/ascii-character-set.md)
  * [Multibyte Characters](../c-language/multibyte-characters.md)
  * [Bits per Character](../c-language/bits-per-character.md)
  * [Character Sets](../c-language/character-sets1.md)
  * [Unrepresented Character Constants](../c-language/unrepresented-character-constants.md)
  * [Wide Characters](../c-language/wide-characters.md)
  * [Converting Multibyte Characters](../c-language/converting-multibyte-characters.md)
  * [Range of char Values](../c-language/range-of-char-values.md)
* #### [Integers](integers.md)
  * [Range of Integer Values](../c-language/range-of-integer-values.md)
  * [Demotion of Integers](../c-language/demotion-of-integers.md)
  * [Signed Bitwise Operations](../c-language/signed-bitwise-operations.md)
  * [Remainders](../c-language/remainders.md)
  * [Right Shifts](../c-language/right-shifts.md)
* #### [Floating point math](floating-point-math.md)
  * [Values](../c-language/values.md)
  * [Casting Integers to Floating-Point Values](../c-language/casting-integers-to-floating-point-values.md)
  * [Truncation of Floating-Point Values](../c-language/truncation-of-floating-point-values.md)
* #### [Arrays and pointers](arrays-and-pointers.md)
  * [Largest Array Size](../c-language/largest-array-size.md)
  * [Pointer Subtraction](../c-language/pointer-subtraction.md)
* #### [Structures, unions, enumerations and bit fields]()
  * [Improper-access-to-a-union](improper-access-to-a-union.md)
  * [Padding and alignment of structure members](padding-and-alignment-of-structure-members.md)
  * [Sign-of-bit-fields](sign-of-bit-fields.md)
  * [Storage-of-bit-fields](storage-of-bit-fields.md)
  * [Enum-type](enum-type.md)
* #### [Preprocessing directives](preprocessing-directives.md)
  * [Character Constants and Conditional Inclusion](../c-language/character-constants-and-conditional-inclusion.md)
  * [Including Bracketed Filenames](../c-language/including-bracketed-filenames.md)
  * [Including Quoted Filenames](../c-language/including-quoted-filenames.md)
  * [Character Sequences](../c-language/character-sequences.md)
  * [Pragmas](../c-language/pragmas.md)
  * [Default Date and Time](../c-language/default-date-and-time.md)
* #### [Library functions](library-functions.md)
  * [NULL Macro](../c-language/null-macro.md)
  * [Diagnostic Printed by the assert Function](../c-language/diagnostic-printed-by-the-assert-function.md)
  * [Character Testing](../c-language/character-testing.md)
  * [Domain Errors](../c-language/domain-errors.md)
  * [Underflow of Floating-Point Values](../c-language/underflow-of-floating-point-values.md)
  * [The fmod Function](../c-language/fmod-function.md)
  * [The signal Function](../c-language/signal-function-c.md)
  * [Default Signals](../c-language/default-signals.md)
  * [Terminating Newline Characters](../c-language/terminating-newline-characters.md)
  * [Blank Lines](../c-language/blank-lines.md)
  * [Null Characters](../c-language/null-characters.md)
  * [File Position in Append Mode](../c-language/file-position-in-append-mode.md)
  * [Truncation of Text Files](../c-language/truncation-of-text-files.md)
  * [File Buffering](../c-language/file-buffering.md)
  * [Zero-Length Files](../c-language/zero-length-files.md)
  * [Filenames](../c-language/filenames.md)
  * [File Access Limits](../c-language/file-access-limits.md)
  * [Deleting Open Files](../c-language/deleting-open-files.md)
  * [Renaming with a Name That Exists](../c-language/renaming-with-a-name-that-exists.md)
  * [Reading Pointer Values](../c-language/reading-pointer-values.md)
  * [Reading Ranges](../c-language/reading-ranges.md)
  * [File Position Errors](../c-language/file-position-errors.md)
  * [Messages Generated by the perror Function](../c-language/messages-generated-by-the-perror-function.md)
  * [Allocating Zero Memory](../c-language/allocating-zero-memory.md)
  * [The abort Function](../c-language/abort-function-c.md)
  * [The atexit Function](../c-language/atexit-function-c.md)
  * [Environment Names](../c-language/environment-names.md)
  * [The system Function](../c-language/system-function.md)
  * [The strerror Function](../c-language/strerror-function.md)
  * [The Time Zone](../c-language/time-zone.md)
  * [The clock Function](../c-language/clock-function-c.md)
