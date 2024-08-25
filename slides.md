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

![mui-meme](./mui-meme.png)

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
layout: center
class: text-center
---

![dropdown-menu](./dropdown-menu.png)

---

## 💡 Discovering Headless Components

- Introduction to Headless Components: Accessible components without styling

<br/>

### Benefits Realized

- **♿ Accessibility**: Pre-built, well-tested components
- **🎨 Flexibility**: Complete control over design and rendering logic - using the power of **inversion of control**
- **🚀 Performance**: Reduced bundle size by importing only what's needed

---

## Available Headless Component Libraries

<br/>

### Radix UI

- Accessible primitives for building high-quality, accessible design systems and web apps.
- Components: Dialog, Dropdown Menu, Tooltip, Slider, and more.


### Headless UI

- Completely unstyled, fully accessible UI components, designed to integrate beautifully with Tailwind CSS.
- Components: Menu, Listbox, Combobox, Switch, Dialog, and more.

<br/>

### Reakit

- Accessible, composable, and reusable components for React.
- Components: Button, Checkbox, Dialog, Menu, Popover, and more.


### Downshift

- Primitives to build simple, flexible, WAI-ARIA compliant enhanced input React components.
- Components: Dropdown, Combobox, Autocomplete, and more.

---

## ⚖️ Pros and Cons of Headless Components

<br/>
<br/>

### Pros:

- Customization: Tailored to unique design and functionality needs
- Bundle Size: Only necessary code is included, reducing bloat
- Styling Freedom: Compatible with any styling solution

<br/>

### Cons:

- Responsibility: More decisions and custom implementation required

---
layout: center
class: text-center
---
## You Own the style

![spiderman](./spiderman.png)



---

## Introducing Shadcn

<br/>
<br/>


- [shadcn/ui](https://ui.shadcn.com/)
- [shadcn/ui themes](https://ui.shadcn.com/themes)

<br/>
<br/>

### shadcn ecosystem
- https://shipixen.com/component-explorer-shadcn

---
layout: center
class: text-center
---
### Tech stack - [create T3 app](https://create.t3.gg/)

![create-t3-app](./create-t3-app.png)

---

![linearB](./linearB.png)

---

## Using Shadcn as the base for engineering metrics

- [v0.dev](https://v0.dev)

- first UI POC was delivered in **1 day**

- working MVP was delivered and less that **3 weeks**

---

## [Engineering Metrics](https://engineering-metrics.nextinsurance.io/)

---

## Credits

[Nir Ben-Yair](https://medium.com/@nirbenyair/headless-components-in-react-and-why-i-stopped-using-ui-libraries-a8208197c268)

---

![9/11](./boom.png)

---
layout: center
class: text-center
---

# 🙏 Thanks


---

## 👋 Thank You

- Q&A
