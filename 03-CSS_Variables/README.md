![App Screenshot](https://github.com/Huiclaire/JavaScript30/blob/master/03-CSS_Variables/image/js30-day3.png)


# 03- CSS Variables and JS

This is an HTML page enable users to edit a photo through CSS variables and filters.

## Demo
view demo [here](https://huiclaire.github.io/JavaScript30/02-JS_and_CSS_Clock/index-Claire.html)

## Lesson learned

- CSS variables
```javascript
:root {
  --base: #ffc600;
  --spacing: 10px;
  --blur: 10px;
}

img {
  padding: var(--spacing);
  background-color: var(--base);
  filter: blur(var(--blur));
}
```

- change CSS property via JS
```javascript
document.documentElement.style.setProperty('--<varName>', '<varValue>')

```
