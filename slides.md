# Unleash the power of Headless Components

---

## 🚀 Introduction

<br/>

### About Me

- **Name:** Yedidya Rashi
- **Role:** DevEx Developer at Next Insurance
- **Passion:** Web development & open-source projects
- **Interests:** Computer science, math, economics, gaming, and wasting my TikTok

---

![engineering metrics](./engineering-metrics.png)

---

## 🏗️ Design System Requirements

<br/>

1. ♿ **Accessibility**
2. 🌓 **Theming**
3. 🎨 **Unique Design**
4. 🌐 **Cross-Browser Support**
5. 🛠️ **Custom Functionality**
6. 📱 **Responsiveness**
7. 🧹 **Maintainability**

---
layout: image-right
image: ./mui-meme.png
backgroundSize: 30em
---

## 🎢 The UI Library Rollercoaster

<br/>


### Stage 1: Exploration
1. **React-Bootstrap**
   - Used for complex components
   - Custom implementation of atomic components

<br/>


2. **Material-UI (MUI)**
   - Modern API and improved theming
   - Integration of best practices
   - Limitation: Struggle with highly custom components

---

## 😅 Stage 2: The Props Jungle

### The Challenge of Custom Components

<br/>

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

```ts {6-7}
const Modal = ({
  isOpen,
  onClose,
  title,
  children,
  width,
  height,
}) {
  ...
};
```

```ts {8}
const Modal = ({
  isOpen,
  onClose,
  title,
  children,
  width,
  height,
  customClassName,
}) {
  ...
};
```

```ts {9-12}
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
}) {
  ...
};
```

```ts
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
  ...
}) {
   // A minimum of 300 lines of logic should be tested for 
   // Custom Functionality, Theming, Accessibility, Cross-Browser Support, Responsiveness, etc.
  ...
};
```
````

<!--
Examples: Autocomplete, Combobox, Multi-tag-select, Dropdown, Modals

Issues: Difficulties in enforcing design and functionality

Conclusion: MUI was not flexible enough for unique needs
-->
---
layout: image-right
image: ./dropdown-menu.png
backgroundSize: 45em
---

# **Key Issues:**
- Prop explosion
- Difficulty in enforcing design consistency
- Limited flexibility for unique needs
- need to test things that we don't want to care about

---

## 💡 The Headless Revolution

<br/>


### Discovering Headless Components

<br/>


**Definition:** Accessible components without pre-defined styling

<br/>

**Key Benefits:**
1. ♿ Built-in accessibility
2. 🎨 Complete design control
3. 🚀 Optimized performance
4. 🧩 Flexible composition

---

## Available Headless Component Libraries

<br/>

## 🛠️ Headless Component Libraries

<br/>

1. **Radix UI**
   - Accessible primitives for robust design systems

2. **Headless UI**
   - Unstyled, accessible components (Tailwind CSS friendly)

3. **Reakit**
   - Composable and reusable React components

4. **Downshift**
   - WAI-ARIA compliant primitives for enhanced inputs

---

## ⚖️ The Headless Trade-off

<br/>
<br/>

### Pros
- Unparalleled customization
- Reduced bundle size
- Styling freedom

<br/>

### Cons
- Increased responsibility for implementation

---
layout: center
class: text-center
---
## You Own the style

![spiderman](./spiderman.png)



---

## 🎨 Shadcn: The Best of Both Worlds

<br/>
<br/>


### Features
- Pre-built, customizable components
- Based on Radix UI
- Themeable and accessible

<br/>
<br/>

### Ecosystem
- [shadcn/ui](https://ui.shadcn.com/)
- [shadcn/ui themes](https://ui.shadcn.com/themes)
- [Shipixen Component Explorer](https://shipixen.com/component-explorer-shadcn)

---

![linearB](./linearB.png)

---

## 🚀 Case Study: Engineering Metrics Dashboard

<br/>

### Tech Stack

- [v0.dev](https://v0.dev)
- [Create T3 App](https://create.t3.gg/)
- Shadcn UI

<br/>

### Development Timeline
- UI Prototype: **1 day**
- Working MVP: **~ 3 weeks**

<br/>

[View the Dashboard](https://engineering-metrics.nextinsurance.io/)

---

## 🎓 Key Takeaways

<br/>

1. Headless components offer unparalleled flexibility
2. Consider the trade-off between customization and development speed
3. Shadcn provides a balanced approach for many projects
4. Always prioritize accessibility and performance

---

## 📚 Further Reading

<br/>


- [Nir Ben-Yair's Article on Headless Components](https://medium.com/@nirbenyair/headless-components-in-react-and-why-i-stopped-using-ui-libraries-a8208197c268)
- [Radix UI Documentation](https://www.radix-ui.com/)
- [Headless UI Guide](https://headlessui.dev/)
- [Create T3 App Documentation](https://create.t3.gg/)

---
layout: center
class: text-center
---

# 🙏 Special Thanks

### Tamir Zur & DevEx team



---

## 👋 Thank You

- Q&A
