## Правила, настоятельно рекомендованные разработчиками ангулара

См. https://angular.io/guide/styleguide


### Содержание

* Codelyzer
  * [x] no-input-rename (0)
  * [ ] no-output-named-after-standard-event (38)
  * [ ] no-output-on-prefix (43)
  * [x] no-output-rename (0)
  * [x] no-unused-css (0) (has fixer)
  * [x] use-life-cycle-interface (0)
  * [x] use-pipe-decorator (0)
  * [x] use-pipe-transform-interface (0)
  * [x] use-view-encapsulation (0)
  * [x] component-class-suffix (0)
  * [x] component-selector (0)
  * [x] directive-class-suffix (0)
  * [x] directive-selector (0)
  * [x] use-host-property-decorator (0)
  * [x] use-input-property-decorator (0)
  * [x] use-output-property-decorator (0)
* Deprecated
  * [x] pipe-naming

### Мнение


### Конфиг

```
"no-input-rename": true,
"no-output-rename": true,
"no-unused-css": true,
"use-life-cycle-interface": true,
"use-pipe-decorator": true,
"use-pipe-transform-interface": true,
"use-view-encapsulation": true,
"component-class-suffix": [true, "Component", "Controller"],
"component-selector": [true, "element", ["app", "ui", "layout", "widget", "chat", "personal", "corporate", "dev", "reactive-form"], "kebab-case"],
"directive-class-suffix": [true, "Directive"],
"directive-selector": [true, "attribute", ["app", "ui", "layout", "widget", "chat", "matomo"], "camelCase"],
"use-host-property-decorator": true,
"use-input-property-decorator": true,
"use-output-property-decorator": true,
```


### Документация

#### + no-input-rename (0)
http://codelyzer.com/rules/no-input-rename

Disallows renaming directive inputs by providing a string to the decorator. See more at (https://angular.io/styleguide#style-05-13).

> "no-input-rename": true


#### no-output-named-after-standard-event (38) (VERSION)
http://codelyzer.com/rules/no-output-named-after-standard-event

Disallows naming directive outputs after a standard DOM event. Listeners subscribed to an output with such a name will also be invoked when the native event is raised.

> "no-output-named-after-standard-event": true


#### no-output-on-prefix (43)
http://codelyzer.com/rules/no-output-on-prefix

Name events without the prefix `on`. See more at (https://angular.io/guide/styleguide#dont-prefix-output-properties).
Angular allows for an alternative syntax on-*. If the event itself was prefixed with on this would result in an on-onEvent binding expression. 

> "no-output-on-prefix": true


#### + no-output-rename (0)
http://codelyzer.com/rules/no-output-rename

Disallows renaming directive outputs by providing a string to the decorator. See more at (https://angular.io/styleguide#style-05-13).

> "no-output-rename": true


#### no-unused-css (0) (has fixer)
http://codelyzer.com/rules/no-unused-css

Disallows having an unused CSS rule in the component’s stylesheet.

> "no-unused-css": true


#### + use-life-cycle-interface (0)
http://codelyzer.com/rules/use-life-cycle-interface

Ensure that components implement life cycle interfaces if they use them. See more at (https://angular.io/styleguide#style-09-01).

> "use-life-cycle-interface": true


#### use-pipe-decorator (0)
http://codelyzer.com/rules/use-pipe-decorator

Ensure that classes implementing PipeTransform interface, use Pipe decorator

> "use-pipe-decorator": true


#### + use-pipe-transform-interface (0)
http://codelyzer.com/rules/use-pipe-transform-interface

Ensure that pipes implement PipeTransform interface.

> "use-pipe-transform-interface": true


#### use-view-encapsulation (5)
http://codelyzer.com/rules/use-view-encapsulation

Disallows using of `ViewEncapsulation.None`

> "use-view-encapsulation": true


#### + component-class-suffix (0)
http://codelyzer.com/rules/component-class-suffix

Classes decorated with `@Component` must have suffix “Component” (or custom) in their name. See more at (https://angular.io/styleguide#style-02-03).
* Supply a list of allowed component suffixes. Defaults to “Component”.

> "component-class-suffix": true
> "component-class-suffix": [true, "Component", "Controller"]


#### + component-selector (0)
http://codelyzer.com/rules/component-selector

Component selectors should follow given naming rules. See more at (https://angular.io/styleguide#style-02-07), (https://angular.io/styleguide#style-05-02), and (https://angular.io/styleguide#style-05-03).
* "element" or "attribute" forces components either to be elements or attributes.
* A single prefix (string) or array of prefixes (strings) which have to be used in component selectors.
* "kebab-case" or "camelCase" allows you to pick a case.

> "component-selector": [true, "element", ["app", "ui", "layout", "widget", "chat", "personal", "corporate", "dev", "reactive-form"], "kebab-case"]


#### + directive-class-suffix (0)
http://codelyzer.com/rules/directive-class-suffix

Classes decorated with @Directive must have suffix “Directive” (or custom) in their name. See more at (https://angular.io/styleguide#style-02-03).
* Supply a list of allowed component suffixes. Defaults to “Directive”.

> "directive-class-suffix": true
> "directive-class-suffix": [true, "Directive"]


#### + directive-selector (0)
http://codelyzer.com/rules/directive-selector

Directive selectors should follow given naming rules. See more at (https://angular.io/styleguide#style-02-06) and (https://angular.io/styleguide#style-02-08).
* "element" or "attribute" forces components either to be elements or attributes.
* A single prefix (string) or array of prefixes (strings) which have to be used in directive selectors.
* "kebab-case" or "camelCase" allows you to pick a case.

> "directive-selector": [true, "attribute", ["app", "ui", "layout", "widget", "chat"], "camelCase"]


#### pipe-naming (0) (DEPRECATED)
http://codelyzer.com/rules/pipe-naming

Enforce consistent case and prefix for pipes. 
* The first item in the array is "kebab-case" or "camelCase", which allows you to pick a case.
* The rest of the arguments are supported prefixes (given as strings). They are optional.

> "pipe-naming": [true, "camelCase"]


#### + use-host-property-decorator (0)
http://codelyzer.com/rules/use-host-property-decorator

Use `@HostProperty` decorator rather than the `host` property of `@Component` and `@Directive` metadata. See more at (https://angular.io/styleguide#style-06-03).

> "use-host-property-decorator": true


#### + use-input-property-decorator (0)
http://codelyzer.com/rules/use-input-property-decorator

Use `@Input` decorator rather than the `inputs` property of `@Component` and `@Directive` metadata. See more at (https://angular.io/styleguide#style-05-12).

> "use-input-property-decorator": true


#### + use-output-property-decorator (0)
http://codelyzer.com/rules/use-output-property-decorator

Use `@Output` decorator rather than the `outputs` property of `@Component` and `@Directive` metadata. See more at (https://angular.io/styleguide#style-05-12).

> "use-output-property-decorator": true


