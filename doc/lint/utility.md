## Правила организации кода и отладки

Тут правила про организацию кода в кучки, и всякие ограничения на использование других кучек кода. И про дебаг, которому место только на локалхостах. И про `eval`, который до добра не доводит. И прочее, жестокое, но нужное. И может даже и не нужное, но сильно полезное.


### Содержание

* Maintainability
  * [ ] cyclomatic-complexity (7)
  * [ ] deprecation (140)
  * [ ] max-classes-per-file (44/44/15)
  * [x] no-duplicate-imports (58)
  * [x] no-mergeable-namespace (0)
  * [x] no-require-imports (0)
* Functionality
  * [ ] ! ban (?)
  * [x] import-blacklist (0) -- `rxjs`
  * [x] no-console (143) 
  * [x] no-debugger (0)
  * [ ] no-dynamic-delete (8)
  * [x] no-eval (0)
  * [x] -no-implicit-dependencies (1650) -- упоротое правило 
  * [x] no-string-throw (0) (has fixer)
* TypeScript-specific
  * [ ] ! ban-types (?)
  * [x] no-internal-module (0) (has fixer)
  * [x] no-namespace (0)
  * [x] no-reference (0)
  * [x] no-var-requires (0)


### Мнение



### Конфиг

#### Сейчас

```
"no-duplicate-imports": true,
"no-mergeable-namespace": true,
"no-require-imports": true,
"import-blacklist": [true, "rxjs"],
"no-console": [true, "debug", "exception", "info", "log", "profile", "profileEnd", "time", "timeEnd", "trace", "warn"],
"no-debugger": true,
"no-eval": true,
"no-implicit-dependencies": false,
"no-string-throw": true,
"ban-types": false,
"no-internal-module": true,
"no-namespace": [true, "allow-declarations"],
"no-reference": true,
"no-var-requires": true,
```

#### Есть автофиксер

```
```

#### Нужно вручную править

```
```

#### Когда-нибудь

```
```

### Документация

#### cyclomatic-complexity (7)
https://palantir.github.io/tslint/rules/cyclomatic-complexity/

Enforces a threshold of cyclomatic complexity.

> "cyclomatic-complexity": [true, 20]


#### deprecation (140)
https://palantir.github.io/tslint/rules/deprecation

Warns when deprecated APIs are used.

> "deprecation": true


#### max-classes-per-file (44/44/15)
https://palantir.github.io/tslint/rules/max-classes-per-file

A file may not contain more than the specified number of classes
* The one required argument is an integer indicating the maximum number of classes that can appear in a file.
* An optional argument "exclude-class-expressions" can be provided to exclude class expressions from the overall class count.

> "max-classes-per-file": [true, 5]
> "max-classes-per-file": [true, 5, "exclude-class-expressions"]
> "max-classes-per-file": [true, 10]


#### no-duplicate-imports (58)
https://palantir.github.io/tslint/rules/no-duplicate-imports

Disallows multiple import statements from the same module.

> "no-duplicate-imports": true


#### no-mergeable-namespace (0)
https://palantir.github.io/tslint/rules/no-mergeable-namespace

Disallows mergeable namespaces in the same file.

> "no-mergeable-namespace": true


#### no-require-imports (0)
https://palantir.github.io/tslint/rules/no-require-imports

Disallows invocation of require().

> "no-require-imports": true


#### ! ban (?)
https://palantir.github.io/tslint/rules/ban

Bans the use of specific functions or global methods.

.....


#### +- import-blacklist (95)
https://palantir.github.io/tslint/rules/import-blacklist

Disallows importing the specified modules directly via import and require. Instead only sub modules may be imported from that module.

> "import-blacklist": [true, "rxjs", "lodash"]


#### +- no-console (143)
https://palantir.github.io/tslint/rules/no-console

Bans the use of specified `console` methods.

> "no-console": true


#### + no-debugger (0)
https://palantir.github.io/tslint/rules/no-debugger

Disallows `debugger` statements.

> "no-debugger": true


#### no-dynamic-delete (8)
https://palantir.github.io/tslint/rules/no-dynamic-delete

Bans usage of the delete operator with computed key expressions.

> "no-dynamic-delete": true


#### + no-eval (0)
https://palantir.github.io/tslint/rules/no-eval

Disallows `eval` function invocations.

> "no-eval": true


#### no-implicit-dependencies (1650) (VERSION)
https://palantir.github.io/tslint/rules/no-implicit-dependencies

Disallows importing modules that are not listed as dependency in the project’s package.json

> "no-implicit-dependencies": [true, "dev"]


#### + no-string-throw (0) (has fixer)
https://palantir.github.io/tslint/rules/no-string-throw

Flags throwing plain strings or concatenations of strings.

> "no-string-throw": true 


#### ! ban-types (?)
https://palantir.github.io/tslint/rules/ban-types

Bans specific types from being used. Does not ban the corresponding runtime objects from being used.
* A list of ["regex", "optional explanation here"], which bans types that match regex

> "ban-types": [true, ["Object", "Use {} instead."], ["String"]]


#### no-internal-module (0) (has fixer)
https://palantir.github.io/tslint/rules/no-internal-module

Disallows internal `module`

> "no-internal-module": true


#### no-namespace (0)
https://palantir.github.io/tslint/rules/no-namespace

Disallows use of internal `module`s and `namespace`s.
* `allow-declarations` allows `declare namespace ... {}` to describe external APIs.

> "no-namespace": [true, "allow-declarations"]


#### no-reference (0)
https://palantir.github.io/tslint/rules/no-reference

Disallows `/// <reference path=>` imports (use ES6-style imports instead).

> "no-reference": true


#### no-var-requires (0)
https://palantir.github.io/tslint/rules/no-var-requires

Disallows the use of require statements except in import statements.

> "no-var-requires": true


