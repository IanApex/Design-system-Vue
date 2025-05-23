# Vue 3 Design System

A comprehensive Vue 3 design system converted from HTML/CSS, featuring reusable components, design tokens, and a complete style guide.

## 🚀 Features

- **Design Tokens**: Centralized color, typography, and spacing variables
- **Vue 3 Components**: Reusable, type-safe components built with Composition API
- **TypeScript Support**: Full TypeScript integration for better development experience
- **Modern Tooling**: Built with Vite for fast development and building
- **Responsive Design**: Mobile-first approach with responsive grid system
- **Accessibility**: Focus states and keyboard navigation support

## 📦 Components

### DSButton
A flexible button component with multiple variants and sizes.

```vue
<DSButton variant="primary" size="large">
  Primary Button
</DSButton>

<DSButton variant="secondary" size="small" :disabled="true">
  Disabled Secondary
</DSButton>
```

**Props:**
- `variant`: `'primary' | 'secondary'` (default: `'primary'`)
- `size`: `'small' | 'large'` (default: `'large'`)
- `disabled`: `boolean` (default: `false`)

### DSBoxInput
Interactive box input component with multiple sizes and states.

```vue
<DSBoxInput 
  size="large" 
  label="Input Label"
  description="Optional description text"
/>

<DSBoxInput 
  size="medium" 
  label="Main Label"
  sideLabel="Side Label"
/>
```

**Props:**
- `size`: `'xs' | 'small' | 'medium' | 'large'` (default: `'small'`)
- `label`: `string` (required)
- `sideLabel`: `string` (optional, for medium size)
- `description`: `string` (optional, for large size)
- `state`: `'default' | 'hover' | 'selected' | 'focus'` (default: `'default'`)

## 🎨 Design Tokens

### Colors
- **Primary**: Green color palette for main actions
- **Neutral**: Grayscale palette for text and backgrounds
- **Accent**: Blue palette for highlights and links
- **Feedback**: Warning and alert colors for status communication

### Typography
- **Font Family**: Roboto (Google Fonts)
- **Font Weights**: Light (300), Regular (400), Medium (500), Bold (700)
- **Type Scale**: H1-H5 headings, body text, and UI element styles

### Spacing
- **Stack Spacing**: Vertical spacing between elements
- **Inline Spacing**: Horizontal spacing between elements
- **Inset Spacing**: Padding variations (all, squish, stretch)

## 🛠️ Development

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Getting Started

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start development server:**
   ```bash
   npm run dev
   ```

3. **Build for production:**
   ```bash
   npm run build
   ```

4. **Type checking:**
   ```bash
   npm run type-check
   ```

### Project Structure

```
src/
├── components/          # Vue components
│   ├── DSButton.vue    # Button component
│   └── DSBoxInput.vue  # Box input component
├── styles/             # CSS files
│   ├── tokens.css      # Design tokens
│   ├── typography.css  # Typography styles
│   ├── button.css      # Button styles
│   ├── inputs.css      # Input styles
│   ├── grid.css        # Grid system
│   ├── spacing.css     # Spacing utilities
│   └── global.css      # Global styles
├── App.vue             # Main app component
├── main.ts             # App entry point
└── style.css           # Main CSS imports
```

## 📚 Usage in Other Projects

### Installation
You can use this design system in other Vue 3 projects by:

1. **Copy the components and styles:**
   ```bash
   # Copy components
   cp -r src/components/* your-project/src/components/
   
   # Copy styles
   cp -r src/styles/* your-project/src/styles/
   ```

2. **Import styles in your main CSS:**
   ```css
   @import './styles/tokens.css';
   @import './styles/typography.css';
   @import './styles/button.css';
   @import './styles/inputs.css';
   @import './styles/grid.css';
   @import './styles/spacing.css';
   @import './styles/global.css';
   ```

3. **Use components in your Vue files:**
   ```vue
   <template>
     <DSButton variant="primary" @click="handleClick">
       Click me
     </DSButton>
   </template>
   
   <script setup>
   import DSButton from '@/components/DSButton.vue'
   
   const handleClick = () => {
     console.log('Button clicked!')
   }
   </script>
   ```

### CSS Custom Properties
All design tokens are available as CSS custom properties:

```css
.my-component {
  background-color: var(--primary-50);
  color: var(--neutral-100);
  padding: var(--spacing-md);
  border-radius: var(--border-radius-md);
}
```

## 🎯 Design Principles

- **Consistency**: Unified visual language across all components
- **Accessibility**: WCAG compliant with proper focus states
- **Scalability**: Modular architecture for easy extension
- **Performance**: Optimized CSS and minimal JavaScript
- **Developer Experience**: TypeScript support and clear documentation

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🔗 Related

- [Vue 3 Documentation](https://vuejs.org/)
- [Vite Documentation](https://vitejs.dev/)
- [TypeScript Documentation](https://www.typescriptlang.org/)
- [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*) 