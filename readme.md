# Fylo Website

Made following a tutorial by Brad Traversy. Site deployed on Netlify: [Fylo Website](https://phenomenal-tapioca-2c319a.netlify.app/ 'Click to visit site')

## What things have I learned working on this project?
+ How to extend tailwind config to include background images, e.g.
```javascript
backgroundImage: () => ({
        'logo-dark-mode': "url('../images/logo-dark-mode.svg')",
        'logo-light-mode': "url('../images/logo-light-mode.svg')",
        'curvy-dark-mode': "url('../images/bg-curvy-dark-mode.svg')",
        'curvy-light-mode': "url('../images/bg-curvy-light-mode.svg')"
      })
```
+ How to extend the same config to be able to toggle light/dark mode by chaning the class of the html root element:
```javascript
module.exports = {
  content: ['./*.html'],
  darkMode: 'class', //this allows us to set class dark on the HTML tag - toggle with JS
  theme: {
  ...
 ```
 + How to toggle between dark and light mode using JS and local storage; here's a code snippet:
 ```javascript
 const toggleDarkMode = function () {
    document.documentElement.classList.toggle("dark");
    if (!localStorage.getItem("theme")) {
      localStorage.setItem("theme", "dark");
    } else {
      localStorage.removeItem("theme");
    }
  };
 ```
 + How cool a color cyan is.
 + How to enable smooth scrolling - as simple as this:
 ```javascript
 <html lang="en" class="scroll-smooth">
 ```

## How would I rate this project?
| Satisfying | Edifying | Total Score |
|------------|----------|-------------|
| 3.5/5      | 3/5      | 3.25/5      |
