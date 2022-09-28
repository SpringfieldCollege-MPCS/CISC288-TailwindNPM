# CISC288-TailwindNPM


# Instructions

** Clone Repository **

1. `git clone https://github.com/SpringfieldCollege-MPCS/CISC288-TailwindNPM.git`
2. `cd CISC288-TailwindNPM`

** Create package.json file and src file(s) **

1. `npm init -y`- create a `package.json` file
2. `npm install -D parcel` - install parcel as a development dependency
3. `mkdir src` - create the the src directory
4. `touch src/index.html` - create the first html file
4. `touch src/index.css` - create the first css file

** Install Tailwind CSS and PostCSS **

1. `npm install -D tailwindcss postcss` - Installs tailwind and postcss
2. `npx tailwindcss init` - creates your tailwind configuration file
3. `touch .postcssrc` - Create an empty configuration file for [postcss](https://postcss.org/).
4. Edit your `.postcssrc` file to be this:
    1. 
    ```
    {
        "plugins": {
            "tailwindcss": {}
        }
    }
    ```
5. Configure your `tailwind.config.js` file:
    1. 
    ```javascript
    /** @type {import('tailwindcss').Config} */
    module.exports = {
    content: [
        "./src/**/*.{html,js,ts,jsx,tsx}",
    ],
    theme: {
        extend: {},
    },
    plugins: [],
    }
    ```

** Edit the HTML File and CSS File **

1. Edit your `src/index.html` file:
    1. 

    ```html
    <!doctype html>
    <html>
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <link href="./index.css" rel="stylesheet">
        </head>
        <body>
            <h1 class="text-3xl font-bold underline">
                Hello world!
            </h1>
        </body>
    </html>
    ```
2. Edit your CSS File

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

*** Run Software ***

1. `npm parcel src/index.html`