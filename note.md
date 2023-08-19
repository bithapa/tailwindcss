> Tailwind CSS is a popular utility-first CSS framework that allows developers to quickly build responsive and customizable user interfaces. It provides a set of pre-designed utility classes that can be directly applied to HTML elements, helping developers avoid writing custom CSS for styling.

* `npm init -y`
    * initialized package.json file

* `npm i -D tailwindcss` Check Documentation: [https://tailwindcss.com/docs/installation](https://tailwindcss.com/docs/installation)
    * adds **tailwind** as dev dependency to the project; `node_modules`

* `npx tailwindcss init`
    * creates Tailwind CSS config file

* Add the Tailwind paths to all of your template files [.html, .js] in your `tailwind.config.js` file.

* **Tailwind CLI Build Process**
    * `npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch`
    * This command will scan our template files for classes and build the CSS into `output.css` file; `input.css` is the input file
    * However we can add our own build script in `package.json` with custom file structure; `--watch` command continuously watches the css classes and builds
        ```
        "scripts": {
            "build": "tailwindcss -i ./input.css -o ./css/main.css",
            "watch": "tailwindcss -i ./input.css -o ./css/main.css --watch"
        }
        ```
    * use `npm run build` to build; creates `css/main.css` directory

---

### File structure

```
TAILWIND:
        |----css
              |----main.css
        |----node_modules
        |----index.html
        |----input.css
        |----notes.md
        |----package-lock.json
        |----package.json
        |----tailwind.config.js    // customize your tailwind css here
```

---

### hsl values

Color model using Hue, Saturation, and Lightness; used as an alternative to the more common `RGB` color model.

See: [W3 School HSL Calculator](https://www.w3schools.com/colors/colors_hsl.asp)