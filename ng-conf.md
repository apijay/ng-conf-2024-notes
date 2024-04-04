# Day 1

## Server side rendering with angular - Alain Chautard
- Repo - https://github.com/alcfeoh/ngx-training/tree/ssr-workshop
- App - https://store.angulartraining.com/#/
- slide - http://bit.ly/at-ssr-workshop

### With angular 17
- ng new --ssr or ng add @angular/ssr
- provideClientHydration() in providers
- It is possible to do parital SSG 
	- discoverRoutes: false
	- routeFiles: "" <- /, /cart, 

## Angular PWAS - Ankita Sood
- Solves software Distribution challenges

### Enterprise Angular app SOS
- PW

## Refactoring codebase with new features

### Strategy
- learn - angular.dev, read code on github, teach someone, learn your project
- Streamline with simplicity
- Try to scope PR and may be use toSignal

### Leverage the framework
- ngSrc
- use esbuild and vite
## NativeScript

# Day 2 

## Manfred session - 10am
- Two way binding - [(ngModel)]=""

- Why Signals
	- Speed up CD

## Architecture Rules
### Synchronusly derive state where possible
### Avoid effects propagating state and signal writes



### Notes
- `#` is ecma standard
- Default value can't be provided for required input signals/models
- `effect()` or `computed()`- Avoid setting the signal 
	- you can do it using {allowSignalWrites: true}
- GlitchFree-ness
- Don't use signal for events but for data
- effect can be only in constructor or a field init
	- Can be lazy by using inject	






























