# Unleash the power of Headless Components

---

## 🚀 Introduction

### About Me

- Yedidya Rashi
- DevEx Developer at Next Insurance
- Passionate about web development and cool open-source projects.
- In my spare time, I enjoy learning about computer science, math, and economics.

---

## 🏗️ Design System Requirements

- **♿ Accessibility**: Ensuring all components are accessible
- **🌓 Theming**: Support for multiple themes (e.g., light/dark mode)
- **🎨 Uniqueness**: Custom look and feel determined by the design team
- **🌐 Browser Support**: Support for all major browsers and IE11
- **🛠️ Functionality**: Custom behaviors tailored to Gloat's unique use cases
- **📱 Responsiveness**: Support for all screen sizes and devices
- **🧹 Maintainability**: Easy to modify and maintain

---

## Stage 1 - 🎢 Journey with UI Libraries

### React-Bootstrap

- Used for complicated components only
- Self-implemented atomic components like Button, Checkbox, Avatar

### Material-UI (MUI)

- Reason: Modern API and better theming support
- Benefits: Hooks, customization, and best practices integration
- Challenge: Struggles with complex custom components

---

## Stage 2 - 😅 The Struggles with Custom Components - Props Jungle

<!-- Examples: Autocomplete, Combobox, Multi-tag-select, Dropdown, Modals
Issues: Difficulties in enforcing design and functionality
Conclusion: MUI was not flexible enough for unique needs -->

````md magic-move {lines: true}
```ts {*|1}
const Modal = ({ isOpen, onClose, title, children }) => {
  if (!isOpen) return null;

  return (
    <div className="modal">
      <div className="modal-header">
        <h2>{title}</h2>
        <button onClick={onClose}>Close</button>
      </div>
      <div className="modal-content">{children}</div>
    </div>
  );
};
```

```ts {7-8}
// prettier-ignore
const Modal = ({
  isOpen,
  onClose,
  title,
  children,
  width,
  height,
})
```

```ts {9}
// prettier-ignore
const Modal = ({
  isOpen,
  onClose,
  title,
  children,
  width,
  height,
  customClassName,
})
```

```ts {10-12}
// prettier-ignore
const Modal = ({
  isOpen,
  onClose,
  title,
  children,
  width,
  height,
  customClassName,
  closeOnOverlayClick,
  onOpen,
  onCloseComplete,
})
```
````

---

## 💡 Discovering Headless Components

- Inspiration: Interaction with a community member, Nick Ribal
- Introduction to Reach UI: Accessible components without styling
- First Impressions: Skepticism due to Reach UI's old-fashioned site

---

## 🤯 Embracing Headless Components

### Finding Headless UI

- Discovery: Through Twitter, led to exploration of Headless UI
- Experimentation: Refactoring Gloat's menu dropdown component

### Benefits Realized

- **♿ Accessibility**: Pre-built, well-tested components
- **🎨 Flexibility**: Complete control over design and rendering logic
- **🚀 Performance**: Reduced bundle size by importing only what's needed

---

## 🏆 Comparing Headless Component Libraries

- **Radix UI**: Well-tested, accessible, but with some React Testing Library issues
- **Reach UI**: Reliable, though with limited components
- **Headless UI**: Best with Tailwind CSS, but less flexible in functionality
- **Downshift**: Total control over styling and functionality, great for complex components
- **Other Libraries**: React-aria, Reakit, Ariakit, and more

---

## ⚖️ Pros and Cons of Headless Components

### Pros:

- Customization: Tailored to unique design and functionality needs
- Bundle Size: Only necessary code is included, reducing bloat
- Styling Freedom: Compatible with any styling solution

### Cons:

- Responsibility: More decisions and custom implementation required
- Community: Smaller, less active than major UI libraries

---

## 🎭 When to Use Headless Components

- Use Case: When building design systems with unique requirements
- Alternative: UI libraries might be better for rapid development without heavy customization needs

---

## 🎬 Conclusion

- Final Thoughts: Headless components offer a balance of flexibility and accessibility
- Recommendation: Consider headless components for projects with unique design demands
- Next Steps: Explore headless components to see if they fit your project's needs

---

## 👋 Thank You

- Q&A Session
