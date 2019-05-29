## Правила форматирования кода

Тут собраны правила, описывающие форматирование кода как текста -- пробелы, кавычки, длина строк и файлов, и прочее низкоуровневое. Всё то, что можно применить к любому языку с аналогичным синтаксисом.


### Содержание

* Style
  * [x] encoding 
  * [x] -file-header (has fixer)
  * [x] file-name-casing (0)
  * [x] import-spacing (0)
  * [ ] newline-before-return (1600)
  * [ ] newline-per-chained-call (1600)
  * [x] no-consecutive-blank-lines (0) (has fixer)
  * [x] no-irregular-whitespace (0) (has fixer)
  * [x] no-trailing-whitespace (0) (has fixer)
  * [x] one-line (0) (has fixer)
  * [x] quotemark (0) (has fixer)
  * [x] semicolon (0) (has fixer)
  * [x] space-before-function-paren (0) (has fixer)
  * [x] space-within-parens (0) (has fixer)
  * [x] whitespace (0) (has fixer)
* Maintainability
  * [x] eofline (0) (has fixer)
  * [x] indent (0) (has fixer)
  * [x] -linebreak-style (?) (has fixer)
  * [x] max-file-line-count (0)
  * [x] max-line-length (0)
* Functionality
  * [x] curly (0) (has fixer)
  * [x] no-invalid-template-strings (0)
* TypeScript-specific
  * [x] typedef-whitespace (0) (has fixer)
* Codelyzer
  * [x] angular-whitespace (0) (has fixer)
  * [x] import-destructuring-spacing (0)


### Мнение

* `encoding` -- проверяет файлы на UTF-8 -- включить на всякий пожарный случай
* `file-header` -- требует комментария в начала файла в спец.формате -- бессмысленный спам, кто их там читает
* `file-name-casing` -- проверяет кейс файлов -- включить `kebab-case`
* `import-spacing` -- требует пробела после `import` -- включить, нужно больше пробелов
* `newline-before-return` -- требует пустой строки перед `return` -- включить, нужно больше пробелов
* `newline-per-chained-call` -- требует перевода строки перед каждым chained-вызовом -- включить, нужно больше пробелов (когда заработает)
* `no-consecutive-blank-lines` -- ограничивает количество последовательных переводов строки -- включить, не более трёх переносов (сильно много пробелов тоже не очень)
* `no-irregular-whitespace` -- запрещает использование любых пробельных символов, кроме \u0020 (пробел) и \u0009 (таб) -- включить, пускай будет
* `no-trailing-whitespace` -- запрещает пробелы в конце строки -- включить, нужно меньше конфликтов при мерже
* `one-line` -- контролирует переносы перед некоторыми ключевыми словами -- включить, не люблю переносы после `}`
* `quotemark` -- контролирует использование кавычек -- включить с запретом на темплейты без интерполяции, люблю простые понятные строки
* `semicolon` -- требует точки с запятой в конце строки -- включить в самом жестоком `always`, потому что нефиг
* `space-before-function-paren` -- контролирует пробел между именем функции и её параметрами (тут есть три варианта -- требовать пробел, требовать отсутствие пробела, игнорировать)
  * анонимные `function () {}` -- требовать пробел
  * нормальные `funcName() {}` -- требовать отсутствие пробела
  * async arrow `async () => {}` -- требовать пробел
  * constructor `constructor() {}` -- требовать отсутствие пробела
  * метод `methodName() {}` -- требовать отсутствие пробела
* `space-within-parens` -- контролирует количество пробелов внутри `()` -- включить 0, не нужно слишком много пробелов
* `whitespace` -- ещё один контроль пробелов
  * "check-branch" -- требует пробел после `if`/`else`/`for`/`while` -- включить
  * "check-decl" -- требует пробел вокруг знака приравнивания -- включить
  * "check-operator" -- требует пробел вокруг знаков операций -- включить
  * "check-module" -- требует пробелы внутри фигурных скобок списков импорта и экспорта -- включить
  * "check-separator" -- требует пробел после символов `,` и `;` -- включить
  * "check-rest-spread" -- требует отсутствие пробела после `...` -- включить
  * "check-type" -- требует пробел перед определением типа переменной `varName: varType` -- включить
  * "check-typecast" -- требует пробел после приведения типа переменной `<varType> varName` -- НЕ включать
  * "check-type-operator" -- требует пробелы вокруг операторов соединения типов `|` и `&`  -- включить
  * "check-preblock" -- требует пробел перед открывающей фигурной скобкой -- включить
* `eofline` -- требует перевод строки в конце файла -- включить, нужно меньше конфликтов при мерже
* `indent` -- определяет формат отступов (на самом деле нет, просто контролирует единообразие таб/пробел) -- включить пробелы, табы зло
* `linebreak-style` -- контролирует формат переводов строк -- не включать, git автоматически исправит всё
* `max-file-line-count` -- контролирует максимальное количество строк в файле -- включить максимум, который есть, затем медленно двигаться хотябы к 1000, а там посмотрим 
* `max-line-length` -- контролирует максимальную длину строки -- оставить как есть и подумать что делать дальше
* `curly` -- требует фигурных скобок у любого блока `if`/`for`/`do`/`while` -- включить, нужно меньше конфликтов при мерже
* `no-invalid-template-strings` -- запрещает `${` в обычных строках -- включить (возможно, это лишний запрет и не тот раздел, но пока других идей нет)
* `typedef-whitespace` -- контролирует пробелы при определении типа (тут есть три варианта -- без пробела, ровно один пробел, любое количество пробелов, и два варианта конфигурации -- до двоеточия и после двоеточия)
  * "call-signature" -- без пробела до, только один пробел после
  * "index-signature" -- без пробела до, только один пробел после
  * "parameter" -- без пробела до, только один пробел после
  * "property-declaration" -- без пробела до, только один пробел после
  * "variable-declaration" -- без пробела до, только один пробел после
* `angular-whitespace` -- контролирует пробелы в шаблонах ангулара -- включить, нужно больше пробелов
* `import-destructuring-spacing` -- опять же требует пробелов в импортах -- включить, забьём последний гвоздь в эту тему


### Конфиг

```
"encoding": true,
"file-header": false,
"file-name-casing": [true, "kebab-case"],
"import-spacing": true,
"no-consecutive-blank-lines": [true, 3],
"no-irregular-whitespace": true,
"no-trailing-whitespace": true,
"one-line": [true, "check-catch", "check-finally", "check-else", "check-open-brace", "check-whitespace"],
"quotemark": [true, "single", "avoid-escape", "avoid-template"],
"semicolon": [true, "always"],
"space-before-function-paren": [true, {"anonymous": "always", "named": "never", "asyncArrow": "always", "constructor": "never", "method": "never"}],
"space-within-parens": [true, 0],
"whitespace": [true, "check-branch", "check-decl", "check-operator", "check-module", "check-separator", "check-rest-spread", "check-type", "check-type-operator", "check-preblock"],
"eofline": true,
"indent": [true, "spaces", 4],
"linebreak-style": false,
"max-file-line-count": [true, 1600],
"max-line-length": [true, 140],
"curly": true,
"no-invalid-template-strings": true,
"typedef-whitespace": [true, {"call-signature": "nospace", "index-signature": "nospace", "parameter": "nospace", "property-declaration": "nospace", "variable-declaration": "nospace"}, {"call-signature": "onespace", "index-signature": "onespace", "parameter": "onespace", "property-declaration": "onespace", "variable-declaration": "onespace"}],
"angular-whitespace": [true, "check-interpolation", "check-semicolon"],
"import-destructuring-spacing": true,
```


#### Нужно вручную править

* `"newline-before-return": true`, 1600 строк

```
"encoding": true,
"file-header": false,
"file-name-casing": [true, "kebab-case"],
"import-spacing": true,
"newline-before-return": true,
"no-consecutive-blank-lines": [true, 3],
"no-irregular-whitespace": true,
"no-trailing-whitespace": true,
"one-line": [true, "check-catch", "check-finally", "check-else", "check-open-brace", "check-whitespace"],
"quotemark": [true, "single", "avoid-escape", "avoid-template"],
"semicolon": [true, "always"],
"space-before-function-paren": [true, {"anonymous": "always", "named": "never", "asyncArrow": "always", "constructor": "never", "method": "never"}],
"space-within-parens": [true, 0],
"whitespace": [true, "check-branch", "check-decl", "check-operator", "check-module", "check-separator", "check-rest-spread", "check-type", "check-type-operator", "check-preblock"],
"eofline": true,
"indent": [true, "spaces", 4],
"linebreak-style": false,
"max-file-line-count": [true, 1600],
"max-line-length": [true, 140],
"curly": true,
"no-invalid-template-strings": true,
"typedef-whitespace": [true, {"call-signature": "nospace", "index-signature": "nospace", "parameter": "nospace", "property-declaration": "nospace", "variable-declaration": "nospace"}, {"call-signature": "onespace", "index-signature": "onespace", "parameter": "onespace", "property-declaration": "onespace", "variable-declaration": "onespace"}],
"angular-whitespace": [true, "check-interpolation", "check-semicolon"],
"import-destructuring-spacing": true,
```


#### Когда-нибудь

* newline-per-chained-call (1600)


### Документация

#### encoding (0)
https://palantir.github.io/tslint/rules/encoding/

Enforces UTF-8 file encoding.

> "encoding": true 


#### - file-header (has fixer)
https://palantir.github.io/tslint/rules/file-header/

Enforces a certain header comment for all files, matched by a regular expression.

.....

> "file-header": false


#### file-name-casing (62) (VERSION)
https://palantir.github.io/tslint/rules/file-name-casing/

Enforces a consistent file naming convention

* camel-case: File names must be camel-cased: fileName.ts.
* pascal-case: File names must be Pascal-cased: FileName.ts.
* kebab-case: File names must be kebab-cased: file-name.ts.

> "file-name-casing": [true, "kebab-case"]


#### import-spacing (0)
https://palantir.github.io/tslint/rules/import-spacing/

Ensures proper spacing between import statement keywords

> "import-spacing": true


#### newline-before-return (1600)
https://palantir.github.io/tslint/rules/newline-before-return

Enforces blank line before return when not the only line in the block.

> "newline-before-return": true


#### newline-per-chained-call (1600) (VERSION)
https://palantir.github.io/tslint/rules/newline-per-chained-call

Requires that chained method calls be broken apart onto separate lines.

> "newline-per-chained-call": true


#### no-consecutive-blank-lines (33) (has fixer)
https://palantir.github.io/tslint/rules/no-consecutive-blank-lines

Disallows one or more blank lines in a row.

> "no-consecutive-blank-lines": [true, 2]


#### no-irregular-whitespace (0) (has fixer)
https://palantir.github.io/tslint/rules/no-irregular-whitespace

Disallow irregular whitespace within a file, including strings and comments.

> "no-irregular-whitespace": true


#### no-trailing-whitespace (0) (has fixer)
https://palantir.github.io/tslint/rules/no-trailing-whitespace

Disallows trailing whitespace at the end of a line.

* "ignore-template-strings": Allows trailing whitespace in template strings.
* "ignore-comments": Allows trailing whitespace in comments.
* "ignore-jsdoc": Allows trailing whitespace only in JSDoc comments.
* "ignore-blank-lines": Allows trailing whitespace on empty lines.

> "no-trailing-whitespace": true


#### one-line (0) (has fixer)
https://palantir.github.io/tslint/rules/one-line

Requires the specified tokens to be on the same line as the expression preceding them.
* "check-catch" checks that catch is on the same line as the closing brace for try.
* "check-finally" checks that finally is on the same line as the closing brace for catch.
* "check-else" checks that else is on the same line as the closing brace for if.
* "check-open-brace" checks that an open brace falls on the same line as its preceding expression.
* "check-whitespace" checks preceding whitespace for the specified tokens.

> "one-line": [true, "check-catch", "check-finally", "check-else", "check-open-brace", "check-whitespace"]


#### quotemark (120) (has fixer)
https://palantir.github.io/tslint/rules/quotemark

Requires single or double quotes for string literals.
* "single" enforces single quotes.
* "double" enforces double quotes.
* "jsx-single" enforces single quotes for JSX attributes.
* "jsx-double" enforces double quotes for JSX attributes.
* "avoid-template" forbids single-line untagged template strings that do not contain string interpolations.
* "avoid-escape" allows you to use the “other” quotemark in cases where escaping would normally be required. For example, [true, "double", "avoid-escape"] would not report a failure on the string literal 'Hello "World"'.

> "quotemark": [true, "single", "avoid-escape", "avoid-template"]


#### semicolon (950) (has fixer)
https://palantir.github.io/tslint/rules/semicolon

Enforces consistent semicolon usage at the end of every statement.

> "semicolon": [true, "always"]


#### space-before-function-paren (69/44/41/7000) (has fixer)
https://palantir.github.io/tslint/rules/space-before-function-paren

Require or disallow a space before function parenthesis
* One argument which is an object which may contain the keys `anonymous`, `named`, and `asyncArrow` These should be set to either "always" or "never".
* "anonymous" checks before the opening paren in anonymous functions
* "named" checks before the opening paren in named functions
* "asyncArrow" checks before the opening paren in async arrow functions
* "method" checks before the opening paren in class methods
* "constructor" checks before the opening paren in class constructors

> "space-before-function-paren": [true, "never"]
> "space-before-function-paren": [true, {"anonymous": "never", "named": "never", "asyncArrow": "never", "constructor": "never", "method": "never"}],
> "space-before-function-paren": [true, {"anonymous": "always", "named": "never", "asyncArrow": "never", "constructor": "never", "method": "never"}]
> "space-before-function-paren": [true, {"anonymous": "always", "named": "never", "asyncArrow": "always", "constructor": "never", "method": "never"}]
> "space-before-function-paren": [true, {"anonymous": "never", "named": "always", "asyncArrow": "never", "constructor": "always", "method": "always"}]


#### space-within-parens (135) (has fixer)
https://palantir.github.io/tslint/rules/space-within-parens

Enforces spaces within parentheses or disallow them. Empty parentheses () are always allowed.

> "space-within-parens": [true, 0]


#### whitespace (770) (has fixer)
https://palantir.github.io/tslint/rules/whitespace

Enforces whitespace style conventions.
* "check-branch" checks branching statements (if/else/for/while) are followed by whitespace.
* "check-decl" checks that variable declarations have whitespace around the equals token.
* "check-operator" checks for whitespace around operator tokens.
* "check-module" checks for whitespace in import & export statements.
* "check-separator" checks for whitespace after separator tokens (,/;).
* "check-rest-spread" checks that there is no whitespace after rest/spread operator (...).
* "check-type" checks for whitespace before a variable type specification.
* "check-typecast" checks for whitespace between a typecast and its target.
* "check-type-operator" checks for whitespace between type operators | and &.
* "check-preblock" checks for whitespace before the opening brace of a block

> "whitespace": [true, "check-branch", "check-decl", "check-operator", "check-module", "check-separator", "check-rest-spread", "check-type", "check-type-operator", "check-preblock"]


#### eofline (0) (has fixer)
https://palantir.github.io/tslint/rules/eofline

Ensures the file ends with a newline.

> "eofline": true


#### indent (0) (has fixer)
https://palantir.github.io/tslint/rules/indent

Enforces indentation with tabs or spaces.
* `spaces` enforces consistent spaces.
* `tabs` enforces consistent tabs.
* A second optional argument specifies indentation size (Indentation size is required for auto-fixing, but not for rule checking):
  * 2 enforces 2 space indentation.
  * 4 enforces 4 space indentation.

> "indent": [true, "spaces", 4]


#### - linebreak-style (?) (has fixer)
https://palantir.github.io/tslint/rules/linebreak-style

Enforces a consistent linebreak style.
* "LF" requires LF (\n) linebreaks
* "CRLF" requires CRLF (\r\n) linebreaks

> "linebreak-style": false


#### max-file-line-count (95/30/6)
https://palantir.github.io/tslint/rules/max-file-line-count

Requires files to remain under a certain number of lines

> "max-file-line-count": [true, 300]
> "max-file-line-count": [true, 500]
> "max-file-line-count": [true, 1000]


#### max-line-length (?)
https://palantir.github.io/tslint/rules/max-line-length

Requires lines to be under a certain max length.
* integer indicating maximum length of lines.
* object with keys:
  * `limit` - number < 0 defining max line length
  * `ignore-pattern` - string defining ignore pattern for this rule, being parsed by new RegExp(). For example:
    * `//` pattern will ignore all in-line comments.
    * `^import` pattern will ignore all import statements.
    * `^export {(.*?)}` pattern will ignore all multiple export statements.
    * `class [a-zA-Z]+ implements` pattern will ignore all class declarations implementing interfaces.
    * `^import |^export {(.*?)}|class [a-zA-Z]+ implements |//` pattern will ignore all the cases listed above.

> "max-line-length": [true, 140]
> "max-line-length": [true, {"limit": 140, "ignore-pattern": "^import |^export {(.*?)}"}]    


#### curly (0) (has fixer)
https://palantir.github.io/tslint/rules/curly

Enforces braces for `if/for/do/while` statements.
* "as-needed" forbids any unnecessary curly braces.
* "ignore-same-line" skips checking braces for control-flow statements that are on one line and start on the same line as their control-flow keyword

> "curly": true


#### no-invalid-template-strings (0)
https://palantir.github.io/tslint/rules/no-invalid-template-strings

Warns on use of `${` in non-template strings.

> "no-invalid-template-strings": true


#### typedef-whitespace (12) (has fixer)
https://palantir.github.io/tslint/rules/typedef-whitespace

Requires or disallows whitespace for type definitions.
* Two arguments which are both objects. The first argument specifies how much space should be to the left of a typedef colon. The second argument specifies how much space should be to the right of a typedef colon. Each key should have a value of "onespace", "space" or "nospace". Possible keys are:
  * "call-signature" checks return type of functions.
  * "index-signature" checks index type specifier of indexers.
  * "parameter" checks function parameters.
  * "property-declaration" checks object property declarations.
  * "variable-declaration" checks variable declaration.

> "typedef-whitespace": [true, {"call-signature": "nospace", "index-signature": "nospace", "parameter": "nospace", "property-declaration": "nospace", "variable-declaration": "nospace"}, {"call-signature": "onespace", "index-signature": "onespace", "parameter": "onespace", "property-declaration": "onespace", "variable-declaration": "onespace"}]


#### angular-whitespace (2150) (has fixer)
http://codelyzer.com/rules/angular-whitespace

Ensures the proper formatting of Angular expressions.
* "check-interpolation" checks for whitespace before and after the interpolation characters
* "check-pipe" checks for whitespace before and after a pipe
* "check-semicolon" checks for whitespace after semicolon

> "angular-whitespace": [true, "check-interpolation", "check-semicolon"]


#### import-destructuring-spacing (2)
http://codelyzer.com/rules/import-destructuring-spacing

Ensure consistent and tidy imports.

> "import-destructuring-spacing": true


