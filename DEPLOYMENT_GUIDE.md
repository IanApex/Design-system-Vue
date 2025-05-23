# 🚀 Deployment & Usage Guide

This guide shows you how to host your Vue Design System as a web reference and use the components in future projects.

## 📡 Hosting Options

### Option 1: Netlify (Recommended - Free & Easy)

1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial Vue Design System"
   git branch -M main
   git remote add origin https://github.com/yourusername/vue-design-system.git
   git push -u origin main
   ```

2. **Deploy to Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repo
   - Build settings are auto-detected from `netlify.toml`
   - Click "Deploy site"
   - Your design system will be live at `https://random-name.netlify.app`

### Option 2: Vercel (Also Free)

1. **Push to GitHub** (same as above)
2. **Deploy to Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Import your GitHub repo
   - Settings are auto-detected from `vercel.json`
   - Your site will be live at `https://your-repo.vercel.app`

### Option 3: GitHub Pages

1. **Enable GitHub Pages:**
   - Go to repo Settings → Pages
   - Source: "GitHub Actions"
   
2. **Create workflow file:**
   ```yaml
   # .github/workflows/deploy.yml
   name: Deploy to GitHub Pages
   on:
     push:
       branches: [ main ]
   jobs:
     build-and-deploy:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - uses: actions/setup-node@v3
           with:
             node-version: '18'
         - run: npm install
         - run: npm run build
         - uses: peaceiris/actions-gh-pages@v3
           with:
             github_token: ${{ secrets.GITHUB_TOKEN }}
             publish_dir: ./dist
   ```

## 🧩 Using Components in Future Projects

### Method 1: Copy Components (Quick Start)

```bash
# In your new Vue project
mkdir src/design-system
cp -r path/to/vue-design-system/src/components/* src/design-system/components/
cp -r path/to/vue-design-system/src/styles/* src/design-system/styles/
```

**In your main CSS file:**
```css
/* src/style.css */
@import './design-system/styles/tokens.css';
@import './design-system/styles/typography.css';
@import './design-system/styles/button.css';
@import './design-system/styles/inputs.css';
@import './design-system/styles/grid.css';
@import './design-system/styles/spacing.css';
@import './design-system/styles/global.css';
```

**Use in components:**
```vue
<template>
  <div>
    <DSButton variant="primary" @click="handleClick">
      Click me!
    </DSButton>
    <DSBoxInput 
      size="large" 
      label="Your Name"
      v-model="name" 
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import DSButton from '@/design-system/components/DSButton.vue'
import DSBoxInput from '@/design-system/components/DSBoxInput.vue'

const name = ref('')
const handleClick = () => console.log('Clicked!')
</script>
```

### Method 2: Create NPM Package (Professional)

1. **Prepare for publishing:**
   ```bash
   # Create package structure
   mkdir vue-design-system-package
   cd vue-design-system-package
   npm init -y
   ```

2. **Create package.json:**
   ```json
   {
     "name": "@yourname/vue-design-system",
     "version": "1.0.0",
     "description": "Vue 3 Design System Components",
     "main": "dist/index.js",
     "module": "dist/index.esm.js",
     "types": "dist/index.d.ts",
     "files": ["dist", "src"],
     "scripts": {
       "build": "rollup -c",
       "dev": "rollup -c -w"
     },
     "peerDependencies": {
       "vue": "^3.0.0"
     },
     "devDependencies": {
       "@rollup/plugin-vue": "^6.0.0",
       "rollup": "^4.0.0",
       "typescript": "^5.0.0"
     }
   }
   ```

3. **Install and use:**
   ```bash
   npm install @yourname/vue-design-system
   ```
   
   ```vue
   <script setup>
   import { DSButton, DSBoxInput } from '@yourname/vue-design-system'
   import '@yourname/vue-design-system/dist/style.css'
   </script>
   ```

### Method 3: Git Submodule (Team Projects)

```bash
# In your new project
git submodule add https://github.com/yourusername/vue-design-system.git src/design-system
git submodule update --init --recursive

# Update design system
git submodule update --remote src/design-system
```

## 🎨 Using Design Tokens

All design tokens are available as CSS custom properties:

```css
.my-component {
  /* Colors */
  background-color: var(--primary-50);
  color: var(--neutral-100);
  border: 1px solid var(--neutral-85);
  
  /* Spacing */
  padding: var(--space-md);
  margin: var(--space-sm);
  gap: var(--space-xs);
  
  /* Typography */
  font-family: var(--font-family-base);
  font-size: var(--font-size-body-lg);
  font-weight: var(--font-weight-medium);
  
  /* Borders & Shadows */
  border-radius: var(--border-radius-md);
  box-shadow: var(--shadow-level-2);
}
```

## 📱 Responsive Breakpoints

```css
/* Mobile first approach */
.component {
  padding: var(--space-sm);
}

@media (min-width: 768px) {
  .component {
    padding: var(--space-md);
  }
}

@media (min-width: 1024px) {
  .component {
    padding: var(--space-lg);
  }
}
```

## 🔧 Customization

### Override Design Tokens
```css
:root {
  /* Override primary colors */
  --primary-50: #your-brand-color;
  --primary-60: #your-brand-color-light;
  
  /* Override spacing */
  --space-md: 20px; /* Instead of 48px */
}
```

### Extend Components
```vue
<!-- MyCustomButton.vue -->
<template>
  <DSButton 
    :class="customClasses"
    v-bind="$attrs"
    @click="$emit('click', $event)"
  >
    <Icon v-if="icon" :name="icon" />
    <slot />
  </DSButton>
</template>

<script setup>
import DSButton from '@/design-system/components/DSButton.vue'

defineProps({
  icon: String,
  customClasses: String
})

defineEmits(['click'])
</script>
```

## 📚 Documentation Site Features

Your hosted design system includes:

- **🎨 Complete Color Palette** - All brand colors with hex values
- **📝 Typography Scale** - Font sizes, weights, and usage examples
- **📏 Spacing System** - Consistent spacing values and names
- **🎯 Interactive Components** - Live button and input examples
- **📖 Code Examples** - Copy-paste ready Vue code
- **🔗 Navigation** - Easy jumping between sections

## 🚀 Next Steps

1. **Deploy your design system** using one of the hosting options
2. **Share the URL** with your team for reference
3. **Start using components** in new projects
4. **Iterate and improve** based on real usage
5. **Consider creating an NPM package** for easier distribution

Your design system is now ready to scale across multiple projects! 🎉 