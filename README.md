# VS Code Typescript Angular/Rxjs/NgRx snippets

[![Version](https://vsmarketplacebadge.apphb.com/version-short/abelfubu.angular-rxjs-ngrx.svg)](https://vsmarketplacebadge.apphb.com/version-short/abelfubu.angular-rxjs-ngrx.svg)
[![Install](https://vsmarketplacebadge.apphb.com/installs/abelfubu.angular-rxjs-ngrx.svg)](https://vsmarketplacebadge.apphb.com/installs/abelfubu.angular-rxjs-ngrx.svg)
[![Downloads](https://vsmarketplacebadge.apphb.com/downloads/abelfubu.angular-rxjs-ngrx.svg)](https://vsmarketplacebadge.apphb.com/downloads/abelfubu.angular-rxjs-ngrx.svg)
[![Ratings](https://vsmarketplacebadge.apphb.com/rating/abelfubu.angular-rxjs-ngrx.svg)](https://vsmarketplacebadge.apphb.com/rating/abelfubu.angular-rxjs-ngrx.svg)

This extension provides you Typescript and Angular/RxJs snippets in Angular for [VS Code](https://code.visualstudio.com/)

## Installation

### Visual Studio Marketplace

Launch _Quick Open_:

- [_Linux_](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf): `Ctrl+P`
- [_macOS_](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf): `⌘P`
- [_Windows_](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf): `Ctrl+P`

Paste the following command and press `Enter`:

```shell
ext install abelfubu.angular-rxjs-ngrx
```

### GitHub Repository Clone

Change to your `.vscode/extensions` [VS Code extensions directory](https://code.visualstudio.com/docs/extensions/install-extension#_side-loading).
Depending on your platform it is located in the following folders:

- _Linux_: `~/.vscode/extensions`
- _macOS_: `~/.vscode/extensions`
- _Windows_: `%USERPROFILE%\.vscode\extensions`

Clone the Material Theme repository as `abelfubu.angular-rxjs-ngrx`:

```shell
git clone https://github.com/abelfubu/angular-rxjs-ngrx.git
```

## Snippets info

Every space inside `{ }` and `( )` means that this is pushed into next line :)
`$` represent each step after `tab`.

## Angular Snippets

|    Prefix | Method                                                    |
| --------: | --------------------------------------------------------- |
|    `ngi→` | `import { Module } from '@angular/folder'`                |
| `ngihcm→` | `import { HttpClientModule } from '@angular/common/http'` |
|   `ngdi→` | `private service: Service`                                |
|   `ngif→` | `*ngIf="condition"`                                       |
|  `ngfor→` | `*ngFor="let variable of array"`                          |

---

### Constructor

`ngcons`

```typescript
constructor(private service: Service) { }
```

### (events)

`nge->`
`ngevent->`
`ngclick->`

```html
(click)="method()"
```

### RouterLink

`ngrl->`

```html
routerLink="/route"
```

### FormGroup

`ngfg->`
`ngformgroup->`

```html
<form [formGroup]="form" (ngSubmit)="onSubmit()">
  <input type="text" formControlName="control" />
</form>
```

### FormControl

`ngfc->`
`ngformcontrol->`

```html
<input type="text" formControlName="control" />
```

### Interface

`ngint->`
`nginterface->`

```typescript
export interface name {
  prop: type;
}
```

### Enum

`ngenum->`

```typescript
export enum name {
  prop = value,
}
```

### Class properties

`ngp->`

```typescript
name: type;
```

### Method

`ngmethod->`

```typescript
name(params): void {

}
```

### FormBuilder

`ngmethod->`

```typescript
this.form = fb.group({
  name: ['', Validators.required],
});
```

### Route

`ngroute->`

```typescript
{ path: name, component: component },
```

## NgRx

### Actions

`ngrxaction->`

```typescript
import { createAction, props } from '@ngrx/store';

export const action = createAction(
  '[type] actionName',
  props<{ prop: type }>()
);
```

### Reducer

`ngrxreducer->`

```typescript
import { createReducer, on } from '@ngrx/store';

export const initialState = {};

const _typeReducer = createReducer(
  initialState,
  on(action, state => state)
);

export function typeReducer(state, action) {
  return _typeReducer(state, action);
}
```

### AppReducer

`ngrxappreducer`

```typescript
import { ActionReducerMap } from '@ngrx/store';
import * as ${1:T} from './$2';

export interface AppState {
  ui: ${1:T}.State;
}

export const appReducers: ActionReducerMap<AppState> = {
  ui: ${1:T}.${3:reducer},
};

// Insert ${4:appReducers} in the app.module imports for StoreModule$0
```

## Angular Material

### MatButton

`matbutton->`

```html
<button mat-raised-button color="accent">
  <mat-icon>menu</mat-icon>
</button>
```

## Autor [Abel de la Fuente -

[Profile](https://abelfubu.github.io/abelfubu-profile/)
[Github](https://github.com/abelfubu)
[Linkedin](https://www.linkedin.com/in/abel-de-la-fuente-53b0291aa/)
