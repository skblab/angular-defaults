## http://codelyzer.com/rules/

### Functionality

* pipe-impure (1) -- и то, там такой пайп, что смысла нет в impure
* templates-no-negated-async (1) (has fixer)
* trackBy-function (290)


#### pipe-impure (1)
http://codelyzer.com/rules/pipe-impure

Pipes cannot be declared as impure

> "pipe-impure": true


#### templates-no-negated-async (1) (has fixer)
http://codelyzer.com/rules/templates-no-negated-async

Ensures that strict equality is used when evaluating negations on async pipe outout. Async pipe evaluate to null before the observable or promise emits, which can lead to layout thrashing as components load. Prefer strict === false checks instead.

> "templates-no-negated-async": true


#### trackBy-function (290)
http://codelyzer.com/rules/trackBy-function

Ensures a TrackBy function is used. Using TrackBy is considired as a best pratice.

> "trackBy-function": true


`max-inline-declarations` which limits the size of inline templates and/or styles. Credits to NagRock #536 174ed46.
`prefer-output-readonly` requires the @Outputs of a component to be readonly. Credits to rafaelss95 #515 3d652d1.
`no-conflicting-life-cycle-hooks` prevents to implement OnChanges and DoCheck on the same class. Credits to rafaelss95 #560 e521115.
`enforce-component-selector` Component Selector Required #551 b9c899b. Credits to wKoza.
`no-life-cycle-call` disallow explicit calls to lifecycle hooks. Credits to rafaelss95 #427 3e10013
`template-cyclomatic-complexity` which limits the estimated Cyclomatic complexity in your templates. Credits to wKoza.
`template-conditional-complexity` which limits the complexity of boolean expressions inside of your templates. Credits to wKoza.

* no-input-prefix	**Stable**
* max-inline-declarations	**Stable**
* prefer-output-readonly	**Stable**
* enforce-component-selector	**Stable**
* no-life-cycle-call	**Stable**
* no-template-call-expression	**Stable**
* no-queries-parameter	**Stable**
* prefer-inline-decorator	**Stable**
* no-conflicting-life-cycle-hooks	**Experimental**
* template-cyclomatic-complexity	**Experimental**
* template-conditional-complexity	**Experimental**
* pipe-prefix
