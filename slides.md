---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## shadcn/ui: Architecture and Implementation
  Presentation slides for developers.
drawings:
  persist: false
transition: slide-left
title: shadcn/ui - Architecture and Implementation
mdc: true
---

# shadcn/ui

Beautifully designed components with a focus on customization and control

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/shadcn/ui" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---

## transition: fade-out

# What is shadcn/ui?

shadcn/ui is a collection of re-usable components that you can copy and paste into your apps

- 🎨 **Beautifully designed** - Clean, modern, and accessible components
- 🛠️ **Customizable** - Tailwind CSS for easy styling
- 📦 **Not a component library** - Copy and paste the components you need
- 🔧 **Flexible** - Use with any framework that supports React
- 🚀 **TypeScript** - Full type safety
- 📄 **Documentation** - Comprehensive guides and examples

<br>

> "The design of your components should be separate from their implementation."

---

## layout: two-cols

# Architecture Overview

shadcn/ui follows a two-layered architecture:

1. Structure and Behavior Layer

   - Implements headless representations
   - Uses established libraries (e.g., Radix UI)
   - Handles complex behaviors (keyboard navigation, WAI-ARIA)

2. Style Layer
   - Uses TailwindCSS for styling
   - Implements Class Variance Authority (CVA) for variant management
   - Utilizes global CSS variables for theming

::right::

<div class="pl-4 mt-12">
  <img src="https://ui.shadcn.com/og.jpg" class="rounded-lg shadow-xl" />
</div>

---

## level: 2

# Key Libraries Used

shadcn/ui leverages several well-established libraries:

- **Radix UI**: For headless UI components (Accordion, Popover, Tabs, etc.)
- **React Hook Form**: For form handling and state management
- **Tanstack React Table**: For table views, including filtering and sorting
- **React Day Picker**: For calendar views and date pickers
- **TailwindCSS**: For styling
- **Class Variance Authority (CVA)**: For managing component variants

---

## layout: two-cols

# Component Example: Badge

```tsx
import * as React from "react";
import { cva, type VariantProps } from "class-variance-authority";
import { cn } from "@/lib/utils";

const badgeVariants = cva(
  "inline-flex items-center rounded-full border px-2.5 py-0.5 text-xs font-semibold transition-colors focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2",
  {
    variants: {
      variant: {
        default:
          "border-transparent bg-primary text-primary-foreground hover:bg-primary/80",
        secondary:
          "border-transparent bg-secondary text-secondary-foreground hover:bg-secondary/80",
        destructive:
          "border-transparent bg-destructive text-destructive-foreground hover:bg-destructive/80",
        outline: "text-foreground",
      },
    },
    defaultVariants: {
      variant: "default",
    },
  }
);

export interface BadgeProps
  extends React.HTMLAttributes<HTMLDivElement>,
    VariantProps<typeof badgeVariants> {}

function Badge({ className, variant, ...props }: BadgeProps) {
  return (
    <div className={cn(badgeVariants({ variant }), className)} {...props} />
  );
}

export { Badge, badgeVariants };
```

::right::

# Key Points

- Uses `cva` for variant management
- Extends HTML `div` attributes
- Utilizes `cn` utility for class merging
- Follows SOLID principles:
  - Single Responsibility
  - Open/Closed
  - Dependency Inversion
- Promotes consistency and reusability

---

## level: 2

# Component Example: Switch

```tsx
import * as React from "react";
import * as SwitchPrimitives from "@radix-ui/react-switch";
import { cn } from "@/lib/utils";

const Switch = React.forwardRef<
  React.ElementRef<typeof SwitchPrimitives.Root>,
  React.ComponentPropsWithoutRef<typeof SwitchPrimitives.Root>
>(({ className, ...props }, ref) => (
  <SwitchPrimitives.Root
    className={cn(
      "peer inline-flex h-6 w-11 shrink-0 cursor-pointer items-center rounded-full border-2 border-transparent transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 focus-visible:ring-offset-background disabled:cursor-not-allowed disabled:opacity-50 data-[state=checked]:bg-primary data-[state=unchecked]:bg-input",
      className
    )}
    {...props}
    ref={ref}
  >
    <SwitchPrimitives.Thumb
      className={cn(
        "pointer-events-none block h-5 w-5 rounded-full bg-background shadow-lg ring-0 transition-transform data-[state=checked]:translate-x-5 data-[state=unchecked]:translate-x-0"
      )}
    />
  </SwitchPrimitives.Root>
));
Switch.displayName = SwitchPrimitives.Root.displayName;

export { Switch };
```

- Uses Radix UI for headless functionality
- Implements keyboard interactions and screen reader support
- Styled using TailwindCSS classes

---

layout: center
class: text-center

---

# Conclusion

shadcn/ui provides a unique approach to component libraries:

- Ownership and control over the code
- Separation of design and implementation
- Leveraging established libraries for complex behaviors
- Flexible styling with TailwindCSS
- Easy customization and extension

[Documentation](https://ui.shadcn.com/docs) · [Components](https://ui.shadcn.com/docs/components/accordion) · [GitHub](https://github.com/shadcn/ui)
