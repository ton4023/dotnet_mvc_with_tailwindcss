npm init -y

npm install tailwindcss postcss autoprefixer postcss-cli

Add a postcss.config.js
// postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}

npx tailwindcss init

Add a style.css under wwwroot/css
//style.css
@tailwind base;
@tailwind components;
@tailwind utilities;

in package.json add
"scripts": {
  "buildcss": "postcss wwwroot/css/style.css -o wwwroot/css/site.css"
},


npm run buildcss