1. npm init -y

2. npm install tailwindcss postcss autoprefixer postcss-cli

3. Add a postcss.config.js
// postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}

4. npx tailwindcss init

5. Add a style.css under wwwroot/css
//style.css
@tailwind base;
@tailwind components;
@tailwind utilities;

6. in package.json add
"scripts": {
  "buildcss": "postcss wwwroot/css/style.css -o wwwroot/css/site.css"
},

7. npm run buildcss