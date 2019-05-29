## Правила форматирования комментариев


### Содержание

* Style
  * [x] comment-format (0) (has fixer) -- можно пообсуждать более подробные варианты
  * [x] -completed-docs
  * [x] -jsdoc-format
  * [x] -no-redundant-jsdoc

### Мнение

Хочется оставить всё как есть. 


### Конфиг

```
"comment-format": [true, "check-space"],
"completed-docs": false,
"jsdoc-format": false,
"no-redundant-jsdoc": false,
```


### Документация

#### +- comment-format (0) (has fixer)

https://palantir.github.io/tslint/rules/comment-format/

Enforces formatting rules for single-line comments.

* "check-space" requires that all single-line comments must begin with a space, as in // comment
  * note that for comments starting with multiple slashes, e.g. ///, leading slashes are ignored
  * TypeScript reference comments are ignored completely
* "check-lowercase" requires that the first non-whitespace character of a comment must be lowercase, if applicable.
* "check-uppercase" requires that the first non-whitespace character of a comment must be uppercase, if applicable.
* Exceptions to "check-lowercase" or "check-uppercase" can be managed with object that may be passed as last argument. One of two options can be provided in this object:
  * `"ignore-words"`  - array of strings - words that will be ignored at the beginning of the comment.
  * `"ignore-pattern"` - string - RegExp pattern that will be ignored at the beginning of the comment.

> "comment-format": [true, "check-space"]


#### - completed-docs

https://palantir.github.io/tslint/rules/completed-docs/

Enforces JSDoc comments for important items be filled out.

.....

> "completed-docs": false


#### - jsdoc-format

https://palantir.github.io/tslint/rules/jsdoc-format

Enforces basic format rules for JSDoc comments.

.....

> "jsdoc-format": false


#### - no-redundant-jsdoc

https://palantir.github.io/tslint/rules/no-redundant-jsdoc

Forbids JSDoc which duplicates TypeScript functionality.

> "no-redundant-jsdoc": false




