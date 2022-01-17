# Installation

1. `npx create-react-app my-app --template [template-name]`

# Adding TailwindCSS

1. `npm install -D tailwindcss postcss autoprefixer`
2. `npx tailwindcss init -p`
3. Edit tailwind.config.js to include `"./src/**/*.{js,jsx,ts,tsx}",` in the contents property
4. Add the following in index.css
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```


