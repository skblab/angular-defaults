
* Style
  * [ ] align (570) (has fixer)
  * [ ] array-type (690) (has fixer)
  * [ ] arrow-parens (2760) (has fixer)
  * [ ] arrow-return-shorthand (160) (has fixer)
  * [ ] binary-expression-operand-order (33)
  * [x] callable-types (0) (has fixer)
  * [x] class-name (0)
  * [ ] interface-name (170/125) -- `always-prefix` / `never-prefix`
  * [x] interface-over-type-literal (0) (has fixer)
  * [ ] new-parens (18)
  * [ ] no-boolean-literal-compare (26) (has fixer)
  * [x] no-reference-import (0)
  * [ ] no-unnecessary-callback-wrapper (4)
  * [x] no-unnecessary-initializer (0) (has fixer)
  * [x] no-unnecessary-qualifier (0) (has fixer)
  * [x] number-literal-format (12)
  * [ ] object-literal-key-quotes (650) (has fixer) -- 650 это для `as-needed`, другие варианты надо проверять
  * [ ] object-literal-shorthand (300) (has fixer) -- очень не хочется приводить всё к этой нотации, она какая-то багогенерящая 
  * [ ] one-variable-per-declaration (14)
  * [ ] ! ordered-imports (?) (has fixer) -- не понимаю, что туда написать, чтобы всем стало хорошо
  * [ ] prefer-function-over-method (575)
  * [ ] prefer-method-signature (8) (has fixer)
  * [ ] prefer-switch (18)
  * [ ] prefer-template (190)
  * [ ] prefer-while (-) (has fixer)
  * [ ] return-undefined (43)
  * [ ] switch-final-break (37) (has fixer)
  * [ ] type-literal-delimiter (125)
  * [x] variable-name (0) -- только `ban-keywords`
* Maintainability
  * [ ] object-literal-sort-keys (2140/1650)
  * [x] prefer-const (0) (has fixer)
  * [ ] prefer-readonly (1800)
  * [ ] trailing-comma (4200/?) (has fixer)
* Functionality
  * [x] no-shadowed-variable (0) -- возможно сейчас слишком строгое правило
  * [x] no-var-keyword (0) (has fixer)  
  

#### align (570) (has fixer)

https://palantir.github.io/tslint/rules/align/

Enforces vertical alignment.

* "parameters" checks alignment of function parameters.
* "arguments" checks alignment of function call arguments.
* "statements" checks alignment of statements.
* "members" checks alignment of members of classes, interfaces, type literal, object literals and object destructuring.
* "elements" checks alignment of elements of array iterals, array destructuring and tuple types.

> "align": [true, "parameters", "arguments", "statements", "members", "elements"]


#### array-type (690) (has fixer)

https://palantir.github.io/tslint/rules/array-type/

Requires using either ‘T[]’ or ‘Array' for arrays.

* "array" enforces use of T[] for all types T.
* "generic" enforces use of Array<T> for all types T.
* "array-simple" enforces use of T[] if T is a simple type (primitive or type reference).

> "array-type": [true, "array-simple"]


#### arrow-parens (2760) (has fixer)

https://palantir.github.io/tslint/rules/arrow-parens/

Requires parentheses around the parameters of arrow function definitions.

* If `ban-single-arg-parens` is specified, then arrow functions with one parameter must not have parentheses if removing them is allowed by TypeScript.

> "arrow-parens": true


#### arrow-return-shorthand (160) (has fixer)

https://palantir.github.io/tslint/rules/arrow-return-shorthand/

Suggests to convert `() => { return x; }` to `() => x`.

* If `multiline` is specified, then this will warn even if the function spans multiple lines.

> "arrow-return-shorthand": [true, "multiline"]


#### binary-expression-operand-order (33)

https://palantir.github.io/tslint/rules/binary-expression-operand-order

In a binary expression, a literal should always be on the right-hand side if possible. For example, prefer ‘x + 1’ over ‘1 + x’.

> "binary-expression-operand-order": true


#### + callable-types (0) (has fixer)

https://palantir.github.io/tslint/rules/callable-types/

An interface or literal type with just a call signature can be written as a function type.

> "callable-types": true


#### + class-name (0)

https://palantir.github.io/tslint/rules/class-name/

Enforces PascalCased class and interface names.

> "class-name": true


#### interface-name (170/125)

https://palantir.github.io/tslint/rules/interface-name

Requires interface names to begin with a capital ‘I’

* "always-prefix" requires interface names to start with an “I”
* "never-prefix" requires interface names to not have an “I” prefix

> "interface-name": [true, "always-prefix"]
> "interface-name": [true, "never-prefix"]


#### + interface-over-type-literal (0) (has fixer)

https://palantir.github.io/tslint/rules/interface-over-type-literal

Prefer an interface declaration over a type literal (type T = { ... })

> "interface-over-type-literal": true


#### new-parens (18)

https://palantir.github.io/tslint/rules/new-parens

Requires parentheses when invoking a constructor via the new keyword.

> "new-parens": true


#### no-boolean-literal-compare (26) (has fixer)

https://palantir.github.io/tslint/rules/no-boolean-literal-compare

Warns on comparison to a boolean literal, as in x === true.

> "no-boolean-literal-compare": true


#### no-reference-import (0)

https://palantir.github.io/tslint/rules/no-reference-import

Don’t `<reference types="foo" />` if you import `foo` anyway.

> "no-reference-import": true


#### no-unnecessary-callback-wrapper (4)

https://palantir.github.io/tslint/rules/no-unnecessary-callback-wrapper

Replaces `x => f(x)` with just `f`. To catch more cases, enable `only-arrow-functions` and `arrow-return-shorthand` too.

> "no-unnecessary-callback-wrapper": true


#### no-unnecessary-initializer (0) (has fixer)

https://palantir.github.io/tslint/rules/no-unnecessary-initializer

Forbids a ‘var’/’let’ statement or destructuring initializer to be initialized to ‘undefined’.

> "no-unnecessary-initializer": true


#### no-unnecessary-qualifier (0) (has fixer)

https://palantir.github.io/tslint/rules/no-unnecessary-qualifier

Warns when a namespace qualifier (`A.x`) is unnecessary.

> "no-unnecessary-qualifier": true


#### number-literal-format (12)

https://palantir.github.io/tslint/rules/number-literal-format

Checks that decimal literals should begin with ‘0.’ instead of just ‘.’, and should not end with a trailing ‘0’.

> "number-literal-format": true


#### object-literal-key-quotes (650) (has fixer)

https://palantir.github.io/tslint/rules/object-literal-key-quotes

Enforces consistent object literal property quote style.

* "always": Property names should always be quoted. (This is the default.)
* "as-needed": Only property names which require quotes may be quoted (e.g. those with spaces in them).
* "consistent": Property names should either all be quoted or unquoted.
* "consistent-as-needed": If any property name requires quotes, then all properties must be quoted. Otherwise, no property names may be quoted.

> "object-literal-key-quotes": [true, "as-needed"]


#### object-literal-shorthand (300) (has fixer)

https://palantir.github.io/tslint/rules/object-literal-shorthand

Enforces/disallows use of ES6 object literal shorthand.
* If the ‘never’ option is provided, any shorthand object literal syntax will cause a failure.

> "object-literal-shorthand": [true, "never"]


#### one-variable-per-declaration (14)

https://palantir.github.io/tslint/rules/one-variable-per-declaration

Disallows multiple variable definitions in the same declaration statement.
* `ignore-for-loop` allows multiple variable definitions in a for loop declaration.

> "one-variable-per-declaration": [true, "ignore-for-loop"]


#### ! ordered-imports (?) (has fixer)

https://palantir.github.io/tslint/rules/ordered-imports

Requires that import statements be alphabetized and grouped.
* Named imports must be alphabetized (i.e. “import {A, B, C} from “foo”;”)
  * The exact ordering can be controlled by the named-imports-order option.
  * “longName as name” imports are ordered by “longName”.
* Import sources must be alphabetized within groups, i.e.: import * as foo from “a”; import * as bar from “b”;
* Groups of imports are delineated by blank lines. You can use these to group imports however you like, e.g. by first- vs. third-party or thematically or can you can enforce a grouping of third-party, parent directories and the current directory.

.....


#### prefer-function-over-method (575)

https://palantir.github.io/tslint/rules/prefer-function-over-method

Warns for class methods that do not use ‘this’.
* “allow-public” excludes checking of public methods. 
* “allow-protected” excludes checking of protected methods.

> "prefer-function-over-method": true


#### prefer-method-signature (8) (has fixer)

https://palantir.github.io/tslint/rules/prefer-method-signature

Prefer `foo(): void` over `foo: () => void` in interfaces and types.

> "prefer-method-signature": true


#### prefer-switch (18)

https://palantir.github.io/tslint/rules/prefer-switch

Prefer a switch statement to an if statement with simple === comparisons.

> "prefer-switch": [true, {"min-cases": 3}]
 

#### prefer-template (190)

https://palantir.github.io/tslint/rules/prefer-template

Prefer a template expression over string literal concatenation.
* If `allow-single-concat` is specified, then a single concatenation (`x + y`) is allowed, but not more (`x + y + z`).

> "prefer-template": [true, "allow-single-concat"]


#### prefer-while (-) (has fixer) (VERSION)

https://palantir.github.io/tslint/rules/prefer-while

Prefer while loops instead of for loops without an initializer and incrementor.

> "prefer-while": true


#### return-undefined (43)

https://palantir.github.io/tslint/rules/return-undefined

Prefer `return;` in void functions and `return undefined;` in value-returning functions.

> "return-undefined": true


#### switch-final-break (37) (has fixer)

https://palantir.github.io/tslint/rules/switch-final-break

Checks whether the final clause of a switch statement ends in break;.

> "switch-final-break": [true, "always"]


#### type-literal-delimiter (125)

https://palantir.github.io/tslint/rules/type-literal-delimiter

Checks that type literal members are separated by semicolons. Enforces a trailing semicolon for multiline type literals.

> "type-literal-delimiter": true


#### +- variable-name (327)

https://palantir.github.io/tslint/rules/variable-name

Checks variable names for various errors.
* "check-format": allows only lowerCamelCased or UPPER_CASED variable names
  * "allow-leading-underscore" allows underscores at the beginning (only has an effect if “check-format” specified)
  * "allow-trailing-underscore" allows underscores at the end. (only has an effect if “check-format” specified)
  * "allow-pascal-case" allows PascalCase in addition to lowerCamelCase.
  * "allow-snake-case" allows snake_case in addition to lowerCamelCase.
* "ban-keywords": disallows the use of certain TypeScript keywords as variable or parameter names.
  * These are: any, Number, number, String, string, Boolean, boolean, Undefined, undefined

> "variable-name": [true, "ban-keywords", "check-format", "allow-leading-underscore"]


#### object-literal-sort-keys (2140/1650)

https://palantir.github.io/tslint/rules/object-literal-sort-keys

Checks ordering of keys in object literals.
* “ignore-case” will compare keys in a case insensitive way.
* “match-declaration-order” will prefer to use the key ordering of the contextual type of the object literal, as in: `interface I { foo: number; bar: number; } const obj: I = { foo: 1, bar: 2 };` If a contextual type is not found, alphabetical ordering will be used instead.
* (VERSION) “shorthand-first” will enforce shorthand properties to appear first, as in: `const obj = { a, c, b: true };`

> "object-literal-sort-keys": true
> "object-literal-sort-keys": [true, "ignore-case", "match-declaration-order"]


#### + prefer-const (0) (has fixer)

https://palantir.github.io/tslint/rules/prefer-const

Requires that variable declarations use const instead of let and var if possible.

.....

> "prefer-const": true


#### prefer-readonly (1800) (VERSION)

https://palantir.github.io/tslint/rules/prefer-readonly

Requires that private variables are marked as readonly if they’re never modified outside of the constructor.
* If only-inline-lambdas is specified, only immediately-declared arrow functions are checked.

> "prefer-readonly": true
> "prefer-readonly": [true, "only-inline-lambdas"]


#### trailing-comma (4200/?) (has fixer)

https://palantir.github.io/tslint/rules/trailing-comma 

Requires or disallows trailing commas in array and object literals, destructuring assignments, function typings, named imports and exports and function parameters.
* One argument which is an object with the keys multiline and singleline. Both can be set to a string ("always" or "never") or an object.
* The object can contain any of the following keys: "arrays", "objects", "functions", "imports", "exports", and "typeLiterals"; each key can have one of the following values: "always", "never", and "ignore". Any missing keys will default to "ignore".
  * "multiline" checks multi-line object literals.
  * "singleline" checks single-line object literals.
* An array is considered “multiline” if its closing bracket is on a line after the last array element. The same general logic is followed for object literals, function typings, named import statements and function parameters.
* To align this rule with the ECMAScript specification that is implemented in modern JavaScript VMs, there is a third option esSpecCompliant. Set this option to true to disallow trailing comma on object and array rest and rest parameters.

> "trailing-comma": [true, {"multiline": "always", "singleline": "never"}]
> "trailing-comma": [true, {"multiline": {"objects": "always", "arrays": "always", "functions": "never", "typeLiterals": "ignore"}, "esSpecCompliant": true}]


#### + no-shadowed-variable (0)
https://palantir.github.io/tslint/rules/no-shadowed-variable

Disallows shadowing variable declarations.

.....

> "no-shadowed-variable": true


#### + no-var-keyword (0) (has fixer)
https://palantir.github.io/tslint/rules/no-var-keyword

Disallows usage of the `var` keyword. Use `let` or `const` instead.

> "no-var-keyword": true


