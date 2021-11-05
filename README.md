# Clon YOUTUBE Vue3 + Tailwind

## Demo

https://alexdolg1967.github.io/my-youtube/

## Отразить изменения на Gihub Pages

in file vite.config.js add base: "link"

```
npm run build

git add dist -f

git commit -m "adding dist"

git subtree push --prefix dist origin gh-pages
```

## Полезности на будущее

Пример анимацииmargin: auto;

```
<transition
	enter-active-class="transition ease-out duration-100"
	enter-from-class="opacity-0 scale-95"
	enter-to-class="opacity-100 scale-100"
	leave-active-class="transition ease-in duration-75"
	leave-from-class="opacity-100 scale-100"
	leave-to-class="opacity-0 scale-95"
>
```

В CSS под "ишака"

```
@media screen and (orientation: landscape) and (max-width: 568px) {
  /* горизонтально  */
  .header { height: 68px; }
  }

@media screen and (-ms-high-contrast: active), (-ms-high-contrast: none) {
   /* IE10 IE11 */
  .c-catalog .c-button {
  	background-color: #FC9F00;
  }
}

```
