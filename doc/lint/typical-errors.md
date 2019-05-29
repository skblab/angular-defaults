## Обязательные правила, контролирующие типовые ошибки

Эти правила запрещают стрелять себе в ногу. Или в ногу соседа. Или вообще стрелять. Ибо нефиг. 


### Содержание

* Functionality
  * [x] label-position (0)
  * [x] no-conditional-assignment (0)
  * [x] no-duplicate-super (0)
  * [x] no-duplicate-switch-case (0)
  * [x] no-duplicate-variable (0)
  * [x] no-misused-new (0)
  * [x] no-switch-case-fall-through (0)
  * [x] no-unsafe-finally (0)
  * [x] radix (0)
  * [x] triple-equals (0)
  * [x] use-isnan (0) 
* TypeScript-specific
  * [x] no-empty-interface (0)
  * [ ] -no-parameter-reassignment (110)
* Codelyzer
  * [x] banana-in-box (0) (has fixer)
  * [x] contextual-life-cycle (0)
  * [x] decorator-not-allowed (0)
  * [x] no-attribute-parameter-decorator (0)


### Мнение



### Конфиг

```
"label-position": true,
"no-conditional-assignment": true,
"no-duplicate-super": true,
"no-duplicate-switch-case": true,
"no-duplicate-variable": [true, "check-parameters"],
"no-misused-new": true,
"no-switch-case-fall-through": true,
"no-unsafe-finally": true,
"radix": true,
"triple-equals": [true, "allow-null-check"],
"use-isnan": true,
"no-empty-interface": true,
"no-parameter-reassignment": false, 
"banana-in-box": true,
"contextual-life-cycle": true,
"decorator-not-allowed": true,
"no-attribute-parameter-decorator": true,
```


### Документация

#### + label-position (0)
https://palantir.github.io/tslint/rules/label-position

This rule only allows labels to be on `do/for/while/switch` statements.

> "label-position": true


#### no-conditional-assignment (2)
https://palantir.github.io/tslint/rules/no-conditional-assignment

Disallows any type of assignment in conditionals. This applies to `do-while`, `for`, `if`, and `while` statements and conditional (ternary) expressions.

> "no-conditional-assignment": true


#### no-duplicate-super (0)
https://palantir.github.io/tslint/rules/no-duplicate-super

Warns if ‘super()’ appears twice in a constructor.

> "no-duplicate-super": true


#### no-duplicate-switch-case (0) (VERSION)
https://palantir.github.io/tslint/rules/no-duplicate-switch-case

Prevents duplicate cases in switch statements.

> "no-duplicate-switch-case": true


#### no-duplicate-variable (0)
https://palantir.github.io/tslint/rules/no-duplicate-variable

Disallows duplicate variable declarations in the same block scope.
* You can specify "check-parameters" to check for variables with the same name as a parameter.

> "no-duplicate-variable": [true, "check-parameters"]


#### no-misused-new (0)
https://palantir.github.io/tslint/rules/no-misused-new

Warns on apparent attempts to define constructors for interfaces or `new` for classes.

> "no-misused-new": true


#### + no-switch-case-fall-through (0)
https://palantir.github.io/tslint/rules/no-switch-case-fall-through

Disallows falling through case statements.

> "no-switch-case-fall-through": true


#### no-unsafe-finally (0)
https://palantir.github.io/tslint/rules/no-unsafe-finally

Disallows control flow statements, such as `return`, `continue`, `break` and `throws` in finally blocks.

> "no-unsafe-finally": true


#### + radix (0)
https://palantir.github.io/tslint/rules/radix

Requires the radix parameter to be specified when calling `parseInt`.

> "radix": true


#### + triple-equals (0)
https://palantir.github.io/tslint/rules/triple-equals

Requires `===` and `!==` in place of `==` and `!=`.
* "allow-null-check" allows == and != when comparing to null.
* "allow-undefined-check" allows == and != when comparing to undefined.

> "triple-equals": true


#### use-isnan (0) 
https://palantir.github.io/tslint/rules/use-isnan

Enforces use of the `isNaN()` function to check for NaN references instead of a comparison to the `NaN` constant.

> "use-isnan": true


#### + no-empty-interface (0)

https://palantir.github.io/tslint/rules/no-empty-interface

Forbids empty interfaces.

> "no-empty-interface": true


#### no-parameter-reassignment (110)

https://palantir.github.io/tslint/rules/no-parameter-reassignment

Disallows reassigning parameters.

> "no-parameter-reassignment": true

 
#### banana-in-box (0) (has fixer)
http://codelyzer.com/rules/banana-in-box

Ensure that the two-way data binding syntax is correct.

> "banana-in-box": true


#### contextual-life-cycle (7)
http://codelyzer.com/rules/contextual-life-cycle

Ensure that classes use allowed life cycle method in its body

> "contextual-life-cycle": true


#### decorator-not-allowed (0)
http://codelyzer.com/rules/decorator-not-allowed

Ensure that classes use allowed decorator in its body

> "decorator-not-allowed": true


#### no-attribute-parameter-decorator (0)
http://codelyzer.com/rules/no-attribute-parameter-decorator

Disallow usage of `@Attribute` decorator. `@Attribute` is considered bad practice. Use `@Input` instead.

> "no-attribute-parameter-decorator": true


