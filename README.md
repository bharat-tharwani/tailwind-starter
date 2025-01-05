# Tailwind Starter Project

A simple starter template to kickstart your Tailwind CSS projects.

## Overview
This project provides the basic setup required to use Tailwind CSS. Follow the steps below to recreate this setup and begin building your Tailwind-based project.

## Steps to Recreate

1. **Initialize the Project**
   Run the following command to create a `package.json` file:
   ```bash
   npm init -y
   ```

2. **Install Tailwind CSS**
   Install Tailwind CSS as a development dependency:
   ```bash
   npm install -D tailwindcss
   ```

3. **Generate Tailwind Configuration File**
   Use the following command to create a `tailwind.config.js` file:
   ```bash
   npx tailwindcss init
   ```

4. **Configure `tailwind.config.js`**
   Modify the `tailwind.config.js` file as needed for your project. Add the paths to your template files under the `content` key. For example:
   ```javascript
   module.exports = {
     content: [
       "./src/*.html",
     ],
     theme: {
       extend: {},
     },
     plugins: [],
   };
   ```

5. **Add Tailwind Directives to Your CSS**
   Create a CSS file (e.g., `input.css`) and include the following Tailwind directives:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

6. **Start the Tailwind CLI Build Process**
   Add the following scripts to your `package.json` file to build and watch your CSS:
   ```json
   "scripts": {
     "build": "tailwindcss -i ./src/input.css -o ./dist/output.css",
     "dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
   }
   ```

   Then, run the desired script to generate the CSS:
   - For production build:
     ```bash
     npm run build
     ```
   - For development watch mode:
     ```bash
     npm run dev
     ```

## Directory Structure
Here’s an example of how your project directory might look:
```
project-root/
├── src/
│   └── input.css
├── css/
│   └── output.css
├── tailwind.config.js
├── package.json
└── node_modules/
```

## Notes
- Ensure you include the generated `output.css` file in your HTML for the styles to take effect.
- Adjust the `content` array in `tailwind.config.js` to match the file types and paths in your project.

## Resources
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Getting Started with Tailwind CSS](https://tailwindcss.com/docs/installation)

Enjoy building your project with Tailwind CSS!
