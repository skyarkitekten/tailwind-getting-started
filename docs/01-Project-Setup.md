# Project Setup

## Steps

1. Create an empty working directory

    ``` bash
    mkdir {project_name}
    ```

1. **Optional:** set up git repo

    ``` bash
    git init
    ```

1. **Optional:** add _node_modules_ to _.gitignore_

    ``` csv
    node_modules
    ```

1. Setup NPM

    ``` bash
    npm init -y
    ```

1. Add core dependencies

    ``` bash
    npm install -D tailwindcss autoprefixer postcss vite
    ```

1. Update the _scripts_ section of _package.json_:

    ``` json
    "scripts": {
        "dev": "vite"
    },
    ```

1. Generate _tailwind.config.js_ and _postcss.config.js_ with the Tailwind CLI:

    ``` bash
    npx tailwind init -p
    ```

1. Add all HTML files to the content section of the _tailwind.config.js_:

    ``` json
    /** @type {import('tailwindcss').Config} */
    module.exports = {
    content: ["*.html"],
    theme: {
        extend: {},
    },
    plugins: [],
    }
    ```

1. Create a standard HTML _index.html_ file in the root of the project. Give it the following _body element_:

    ``` html
    <html lang="en">

    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>

    <body>
        <h1>Hello World</h1>
    </body>

    </html>
    ```

1. Create a standard CSS _main.cs_ file in a subfolder _css_ of the project (e.g. `./css/main.css`). Give it the following content:

    ``` css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

1. Import the stylesheet into the _index.html_ file:

    ``` html
    <head>
        ...
        <link rel="stylesheet" href="./css/main.css">
        ...
    </head>
    ```

1. Add Tailwind CSS styling to the `<h1/>` tag:

    ``` html
    <h1 class="text-red-600 font-sans font-bold">Hello World</h1>
    ```
