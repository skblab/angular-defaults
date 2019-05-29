## Правила, отключенные по разным соображениям

Некоторые ломают код, написанный по официальным рекомендациям angular'а. Некоторые приносят непонятное для angular'а ограничение. Некоторые просто странные. 

### Содержание

* Style
  * [x] -match-default-export-name (1) -- очень странное требование
  * [x] -no-angle-bracket-type-assertion (135) (has fixer) -- спецмагия про ограничения `.tsx`
  * [x] -no-parameter-properties (1730) -- все конструкторы обваливаются
* Maintainability
  * [x] -no-default-export (1) -- зачем оно, непонятно
* Functionality
  * [x] -no-submodule-imports (2400/1600) -- почти всё в исключениях
  * [x] -no-use-before-declare (0) -- не включать, так как forwardRef не работает
  * [x] -strict-type-predicates (-) -- strict-type-predicates does not work without --strictNullChecks
* TypeScript-specific
  * [x] -no-import-side-effect (200) -- отваливается rxjs (возможно, получится использовать для отлавливания лишних импортов rxjs за пределами глобальных, но есть же поиск)
* Codelyzer
  * [x] -i18n (?) -- нам не нужно
  * [x] -no-forward-ref (67) -- зачем-то в лоб ломает элементы форм


### Мнение


### Конфиг

```
"match-default-export-name": false,
"no-angle-bracket-type-assertion": false,
"no-parameter-properties": false,
"no-default-export": false,
"no-submodule-imports": false,
"no-use-before-declare": false,
"strict-type-predicates": false,
"no-import-side-effect": false,
"i18n": false,
"no-forward-ref": false,
```


### Документация

#### match-default-export-name (1)
https://palantir.github.io/tslint/rules/match-default-export-name

Requires that a default import have the same name as the declaration it imports. Does nothing for anonymous default exports.

> "match-default-export-name": true


#### no-angle-bracket-type-assertion (135) (has fixer)
https://palantir.github.io/tslint/rules/no-angle-bracket-type-assertion

Requires the use of `as Type` for type assertions instead of `<Type>`.

> "no-angle-bracket-type-assertion": true


#### no-parameter-properties (1730)
https://palantir.github.io/tslint/rules/no-parameter-properties

Disallows parameter properties in class constructors.

> "no-parameter-properties": true


#### no-default-export (1)
https://palantir.github.io/tslint/rules/no-default-export

Disallows default exports in ES6-style modules. Use named exports instead.

> "no-default-export": true


#### no-submodule-imports (2400/1600)
https://palantir.github.io/tslint/rules/no-submodule-imports

Disallows importing any submodule.
* A list of whitelisted package or submodule names.

> "no-submodule-imports": true
> "no-submodule-imports": [true, "rxjs", "@angular/platform-browser", "@angular/core/testing"]


#### + no-use-before-declare (470/0)
https://palantir.github.io/tslint/rules/no-use-before-declare

Disallows usage of variables before their declaration.

> "no-use-before-declare": true
> "no-use-before-declare": false


#### ! strict-type-predicates (-) -- strict-type-predicates does not work without --strictNullChecks
https://palantir.github.io/tslint/rules/strict-type-predicates

Warns for type predicates that are always true or always false. Works for ‘typeof’ comparisons to constants (e.g. ‘typeof foo === “string”’), and equality comparison to ‘null’/’undefined’. (TypeScript won’t let you compare ‘1 === 2’, but it has an exception for ‘1 === undefined’.) Does not yet work for ‘instanceof’. Does not warn for ‘if (x.y)’ where ‘x.y’ is always truthy. For that, see strict-boolean-expressions.

> "strict-type-predicates": true


#### no-import-side-effect (200)
https://palantir.github.io/tslint/rules/no-import-side-effect

Avoid import statements with side-effect.
* `ignore-module` allows to specify a regex and ignore modules which it matches.

> "no-import-side-effect": true


#### - i18n (?)
http://codelyzer.com/rules/i18n

Ensures following best practices for i18n.
* "check-id" Makes sure i18n attributes have ID specified
* "check-text" Makes sure there are no elements with text content but no i18n attribute

> "i18n": [true, "check-id"]


#### no-forward-ref (67)
http://codelyzer.com/rules/no-forward-ref

Disallows usage of forward references for DI. The flow of DI is disrupted by using `forwardRef` and might make code more difficult to understand.

> "no-forward-ref": true


