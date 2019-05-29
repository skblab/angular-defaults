## https://www.npmjs.com/package/rxjs-tslint-rules

### Содержание

* [ ] rxjs-add
* [ ] rxjs-ban-observables	
* [ ] rxjs-ban-operators	
* [ ] rxjs-deep-operators	
* [x] -rxjs-finnish	
* [ ] rxjs-just	
* [ ] rxjs-no-add	
* [ ] rxjs-no-create	
* [ ] rxjs-no-deep-operators	
* [ ] rxjs-no-do	
* [ ] rxjs-no-finnish	
* [ ] rxjs-no-ignored-error	
* [ ] rxjs-no-ignored-subscribe	
* [x] rxjs-no-internal	
* [ ] rxjs-no-operator	
* [ ] rxjs-no-patched	
* [x] rxjs-no-subject-unsubscribe	
* [ ] rxjs-no-subject-value	
* [ ] rxjs-no-tap	
* [ ] rxjs-no-unbound-methods	
* [x] rxjs-no-unsafe-catch	
* [ ] rxjs-no-unsafe-first	
* [ ] rxjs-no-unsafe-scope	
* [x] rxjs-no-unsafe-switchmap	
* [x] rxjs-no-unsafe-takeuntil	
* [ ] rxjs-no-unused-add	
* [x] rxjs-no-wholesale	
* [ ] rxjs-prefer-observer	
* [ ] rxjs-throw-error	


### Мнение


### Конфиг

```
"rxjs-no-unsafe-takeuntil": true,
"rxjs-no-wholesale": true,
"rxjs-no-subject-unsubscribe": true,
"rxjs-no-internal": true,
"rxjs-no-unsafe-catch": true,
"rxjs-no-unsafe-switchmap": true,
"rxjs-finnish": {"options": [{"functions": false, "methods": false, "parameters": false, "properties": false, "variables": false}], "severity": "error"}
```


### Документация

> WARNING: Before configuring any of the following rules, you should ensure that TSLint's `no-unused-variable` rule is not enabled in your configuration (or in any configuration that you extend). That rule has caused problems in the past - as it leaves the TypeScript program in an unstable state - and has a significant number of still-open issues. Consider using the `no-unused-declaration` rule from `tslint-etc` instead.

#### rxjs-add
Enforces the importation of patched observables and operators used in the module.

The rxjs-add rule takes an optional object with the property `file`. This is the path of the module - relative to the tsconfig.json - that imports the patched observables and operators.


#### rxjs-ban-observables	
Disallows the use of banned observables.


#### rxjs-ban-operators	
Disallows the use of banned operators.


#### rxjs-deep-operators	
Enforces deep importation from within `rxjs/operators` - e.g. `rxjs/operators/map`. Until Webpack does not require configuration for tree shaking to work, there will be situations where deep imports are preferred.	


#### rxjs-finnish	
Enforces the use of Finnish notation.

The rxjs-finnish rule takes an optional object with optional `functions`, `methods`, `parameters`, `properties` and `variables` properties.


#### rxjs-just	
Enforces the use of a `just` alias for `of`. Some other Rx implementations use `just` and if that's your preference, this is the rule for you. (There was some discussion about deprecating `of` in favour of `just`, but it was decided to stick with `of`.) This rule includes a fixer.	


#### rxjs-no-add	
Disallows the importation of patched observables and operators.	


#### rxjs-no-create	
Disallows the calling of `Observable.create`. Use `new Observable` instead.	


#### rxjs-no-deep-operators	
Disallows deep importation from `rxjs/operators`. Deep imports won't be in available in RxJS v6.	


#### rxjs-no-do	
I do without `do` operators. Do you not? Well, `do` isn't always a code smell, but this rule can be useful as a warning.	


#### rxjs-no-finnish	
Disallows the use of Finnish notation.	


#### rxjs-no-ignored-error	
Disallows the calling of `subscribe` without specifying an error handler.	


#### rxjs-no-ignored-subscribe	
Disallows the calling of subscribe without specifying arguments.	


#### rxjs-no-internal	
Disallows importation from `rxjs/internal`.	


#### rxjs-no-operator	
Disallows importation from `rxjs/operator`. Useful if you prefer 'pipeable' operators - which are located in the `operators` directory.	


#### rxjs-no-patched	
Disallows the calling of patched methods. Methods must be imported and called explicitly - not via `Observable` or `Observable.prototype`.	


#### rxjs-no-subject-unsubscribe	
Disallows calling the `unsubscribe` method of a `Subject` instance. For an explanation of why this can be a problem, see this Stack Overflow answer.	


#### rxjs-no-subject-value	
Disallows accessing the `value` property of a `BehaviorSubject` instance.	


#### rxjs-no-tap	
An alias for `rxjs-no-do`.	


#### rxjs-no-unbound-methods	
Disallows the passing of unbound methods as callbacks.	


#### rxjs-no-unsafe-catch	
Disallows unsafe `catch` and `catchError` usage in NgRx effects and `redux-observable` epics.	


#### rxjs-no-unsafe-first	
Disallows unsafe `first` and `take` usage in NgRx effects and `redux-observable` epics.	


#### rxjs-no-unsafe-scope	
Disallows the use of variables/properties from unsafe/outer scopes in operator callbacks.	


#### rxjs-no-unsafe-switchmap	
Disallows unsafe `switchMap` usage in NgRx effects and `redux-observable` epics.	


#### rxjs-no-unsafe-takeuntil	
Disallows the application of operators after `takeUntil`. Operators placed after `takeUntil` can effect subscription leaks.	


#### rxjs-no-unused-add	
Disallows the importation of patched observables or operators that are not used in the module.	


#### rxjs-no-wholesale	
Disallows the wholesale importation of `rxjs` or `rxjs/Rx`.	


#### rxjs-prefer-observer	
Enforces the passing of observers to `subscribe` and `tap`. See this RxJS issue.	


#### rxjs-throw-error	
Enforces the passing of `Error` values to `error` notifications.	

