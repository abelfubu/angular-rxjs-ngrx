# VS Code Typescript Angular/Rxjs/NgRx snippets

[![Version](https://vsmarketplacebadge.apphb.com/version-short/abelfubu.abelfubu-dark.svg)](https://vsmarketplacebadge.apphb.com/version-short/abelfubu.abelfubu-dark.svg)
[![Install](https://vsmarketplacebadge.apphb.com/installs/abelfubu.abelfubu-dark.svg)](https://vsmarketplacebadge.apphb.com/installs/abelfubu.abelfubu-dark.svg)
[![Downloads](https://vsmarketplacebadge.apphb.com/downloads/abelfubu.abelfubu-dark.svg)](https://vsmarketplacebadge.apphb.com/downloads/abelfubu.abelfubu-dark.svg)
[![Ratings](https://vsmarketplacebadge.apphb.com/rating/abelfubu.abelfubu-dark.svg)](https://vsmarketplacebadge.apphb.com/rating/abelfubu.abelfubu-dark.svg)

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

## NgRx

### Actions

`ngact->` `ngrxaction->`

```typescript
import { createAction } from '@ngrx/store';

export const action = createAction('[type] action ');
```

### Reducer

`ngred->` `ngrxred->`

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

## Autor

[Abel de la Fuente - Profile](https://abelfubu.github.io/abelfubu-profile/)

[Github](https://github.com/abelfubu)

[Linkedin](https://www.linkedin.com/in/abel-de-la-fuente-53b0291aa/)