# Setup
```bash
#install node 
nvm install v22.16.0
nvm use v22.16.0 

#create new project
npx @angular/cli@21.2 new [app_name]
cd [app_name]
npm run start
```


# style and class binding
```scss
/* Global */
html {
  font-size: 10px;
}

* {
  box-sizing: border-box;
  font-size: 2rem;
}

h1 {
  font-size: 3rem;
  text-align: center;
  color: rgb(70, 70, 70);
}
input {
  padding: 0.5rem 1.2rem;
  border-radius: 0.5rem;
  font-size: 2rem;
  min-width: 400px;
}

button {
  padding: 0.5rem 1.2rem;
  border-radius: 0.5rem;
  color: white;
  font-size: 2rem;
  &:not(:disabled) {
    cursor: pointer;
  }
}

/* colors */
.red {
  color: red;
}
.blue {
  color: blue,
}
.green {
  color: green,
}
```
```html
<p class="red">test color</p>
<div>
  <button>red</button>
  <button>green</button>
  <button>blue</button>
</div>
```

```ts
color = 'black';
setColor(color: string) {
  this.color = color;
}
```

# Control Flow
## @if
```ts
isLoggedIn = false;
toggleLogin() {
  this.isLoggedIn = !this.isLoggedIn;
}
```

```html
<p>Please Login</p>
<p>Welcome Back!</p>
<button (click)="toggleLogin()">Toggle Login</button>
````

## @for
```ts
 countries = [
  { flag: '🇫🇷', name: 'France' },
  { flag: '🇩🇪', name: 'Germany' },
  { flag: '🇮🇹', name: 'Italy' },
  { flag: '🇪🇸', name: 'Spain' },
  { flag: '🇵🇹', name: 'Portugal' }
];
```

```html
<p>[🇫🇷] France</p>
```