# Skeleton Theme with DaisyUI 5

A modern Shopify theme starter built with DaisyUI 5 and Tailwind CSS, providing a solid foundation for creating beautiful, responsive e-commerce stores.

## 🚀 Features

- **DaisyUI 5.1.12 Integration**: Modern component library with semantic CSS classes
- **Tailwind CSS 4.1.13**: Latest utility-first CSS framework with CSS-based configuration
- **Modern Shopify Architecture**: Follows latest Shopify theme development best practices
- **Responsive Design**: Mobile-first approach with DaisyUI components
- **Theme Switching**: Built-in theme switcher with local storage persistence
- **PostCSS Build Process**: Modern build system optimized for Tailwind CSS v4
- **Developer Friendly**: Easy to customize and extend

## 📦 What's Included

### DaisyUI Components
- Hero sections
- Navigation bars
- Cards and features
- Buttons and forms
- Theme switcher
- All DaisyUI component classes

### Shopify Theme Structure
- Modern section-based architecture
- Reusable snippets and blocks
- Settings schema with theme selection
- Optimized CSS compilation

## 🛠 Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd skeleton-theme
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Build the CSS**
   ```bash
   npm run build
   ```

4. **Development mode (with file watching)**
   ```bash
   npm run dev
   ```

## 📝 Tailwind CSS v4 + DaisyUI 5.1.12

This theme uses the **latest Tailwind CSS v4.1.13** with **DaisyUI 5.1.12**:

- **Cutting Edge**: Latest versions with modern CSS-based configuration
- **PostCSS Build**: Uses `@tailwindcss/postcss` for optimal build process
- **CSS Configuration**: Uses `@theme` directive instead of `tailwind.config.js`
- **Modern Syntax**: `@import "tailwindcss"` and `@plugin "daisyui"` approach
- **Optimized Output**: Improved CSS generation and smaller bundles
- **Future Ready**: Built with the latest web standards

The migration follows the [official Tailwind CSS v4 upgrade guide](https://tailwindcss.com/docs/upgrade-guide) for maximum compatibility.

## 🎨 Available Themes

The theme includes 2 essential DaisyUI themes for a clean, focused experience:

- **Light**: Clean, bright theme perfect for daytime browsing
- **Dark**: Elegant dark theme for low-light environments

This simplified approach ensures consistent branding while providing essential light/dark mode functionality.

## 🔧 Development

### Scripts

- `npm run dev` - Watch for changes and rebuild CSS using PostCSS
- `npm run build` - Build optimized CSS for production with PostCSS
- `npm run build-dev` - Build CSS for development using PostCSS

### File Structure

```
skeleton-theme/
├── assets/
│   ├── styles.css           # Tailwind CSS v4 source with @theme config
│   └── critical.css         # Generated Tailwind v4 + DaisyUI CSS
├── sections/
│   ├── hero-daisyui.liquid  # Hero section with DaisyUI
│   ├── features-daisyui.liquid # Features section
│   └── header.liquid        # Updated header with DaisyUI navbar
├── snippets/
│   ├── theme-switcher.liquid # DaisyUI theme switcher component
│   └── css-variables.liquid # CSS variables and theme logic
├── postcss.config.js       # PostCSS configuration for Tailwind v4
└── package.json           # Dependencies and scripts
```

### Creating New Components

1. **Using DaisyUI classes in sections:**
   ```liquid
   <div class="hero min-h-screen bg-base-200">
     <div class="hero-content text-center">
       <div class="max-w-md">
         <h1 class="text-5xl font-bold">{{ section.settings.title }}</h1>
         <p class="py-6">{{ section.settings.description }}</p>
         <button class="btn btn-primary">Get Started</button>
       </div>
     </div>
   </div>
   ```

2. **After creating new components, rebuild CSS:**
   ```bash
   npm run build
   ```

   Note: Tailwind CSS v4 uses CSS-based configuration with the `@theme` directive in your CSS file instead of a separate config file.

## 🎛 Theme Customization

### Changing DaisyUI Theme

1. **Via Shopify Admin:**
   - Go to Online Store > Themes > Customize
   - Navigate to Theme settings > Colors
   - Select a DaisyUI theme from the dropdown

2. **Via Theme Switcher:**
   - Use the theme switcher component in the header
   - Changes are saved to localStorage

3. **Programmatically:**
   ```javascript
   window.switchDaisyUITheme('dark');
   ```

### Customizing Colors

You can add custom themes by modifying the theme configuration in `tailwind.config.js`:

```javascript
daisyui: {
  themes: [
    "light",
    "dark",
    {
      mytheme: {
        "primary": "#a991f7",
        "secondary": "#f6d860", 
        "accent": "#37cdbe",
        "neutral": "#3d4451",
        "base-100": "#ffffff",
        "base-200": "#f2f2f2",
        "base-300": "#e5e6e6",
        "base-content": "#1f2937",
        // ... other colors
      },
    },
  ],
}
```

## 🧩 Component Examples

### Hero Section
```liquid
<!-- Use the hero-daisyui section -->
{% section 'hero-daisyui' %}
```

### Feature Cards
```liquid
<!-- Use the features-daisyui section -->
{% section 'features-daisyui' %}
```

### Theme Switcher
```liquid
<!-- Add theme switcher anywhere -->
{% render 'theme-switcher', label: 'Switch Theme', size: 'md' %}
```

### Custom Button
```liquid
<button class="btn btn-primary btn-lg">
  Add to Cart
</button>
```

## 📚 Resources

- [DaisyUI Documentation](https://daisyui.com/)
- [Tailwind CSS Documentation](https://tailwindcss.com/)
- [Shopify Theme Development](https://shopify.dev/themes)
- [Shopify Liquid Documentation](https://shopify.dev/api/liquid)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## 🙋‍♂️ Support

For support and questions:
- Check the [Issues](../../issues) section
- Review the [Shopify Community Forums](https://community.shopify.com/)
- Consult the [DaisyUI Documentation](https://daisyui.com/)

---

**Happy theming!** 🎨