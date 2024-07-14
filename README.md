npm create vite@latest

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/my-vue-app.git
git push -u origin main


npm install --save-dev gh-pages


// vite.config.js
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
  plugins: [vue()],
  base: '/my-vue-app/' // Replace 'my-vue-app' with the name of your GitHub repository
})


Update package.json:

"homepage": "https://YOUR_USERNAME.github.io/my-vue-app",
"scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "deploy": "gh-pages -d dist"
  },


npm run build
npm run deploy                // Automatically published git repository. Please wait for update. 
