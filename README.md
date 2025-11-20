# Expo NativeWind Starter - React Native Template 🚀

A premium **React Native Starter Template** built with **Expo Router**, **NativeWind** (Tailwind CSS), and **React Native Reusables**. This template provides a robust, production-ready foundation for building modern, beautiful, and responsive mobile applications with ease.

## 🌟 Features

- **⚡️ Expo Router**: The standard for file-based routing in React Native, making navigation intuitive, deep-linkable, and powerful.
- **💨 NativeWind (Tailwind CSS)**: Style your components using utility classes, just like on the web. Includes full support for **CSS variables** and **Dark Mode**.
- **🧩 React Native Reusables**: Pre-configured, accessible UI components based on **shadcn/ui**, including Accordion, Icons, and more.
- **✨ Animations**: Integrated `tailwindcss-animate` for smooth, utility-first animations.
- **🌑 Dark Mode Ready**: Class-based dark mode support with CSS variables defined in `global.css`.
- **🛠️ Developer Experience**: Path aliases (`@/*`), TypeScript support, and `cn` utility for class merging.
- **📱 Universal**: Build for Android, iOS, and Web from a single codebase.

## 🚀 Getting Started

### 1. Installation

```bash
npm install
```

### 2. Run the Project

```bash
npx expo start
```

- Press `a` for Android (emulator required).
- Press `i` for iOS (simulator required).
- Press `w` for Web.

## 🛠️ Tech Stack & Configuration

This project comes pre-configured with the best tools in the React Native ecosystem:

- **Framework**: [Expo](https://expo.dev) (SDK 52+)
- **Routing**: [Expo Router](https://docs.expo.dev/router/introduction)
- **Styling**: [NativeWind v4](https://www.nativewind.dev/) & [Tailwind CSS](https://tailwindcss.com/)
- **UI Library**: [React Native Reusables](https://rnr-docs.vercel.app/) (shadcn/ui for React Native)
- **Icons**: `lucide-react-native` with `className` support
- **Utils**: `clsx` and `tailwind-merge` for conditional styling

## 🎨 UI Components

This template includes a setup for **React Native Reusables** (based on shadcn/ui).

### Example: Accordion

```tsx
import {
  Accordion,
  AccordionItem,
  AccordionTrigger,
  AccordionContent,
} from "@/components/ui/accordion";

<Accordion type="single" collapsible>
  <AccordionItem value="item-1">
    <AccordionTrigger>Is it accessible?</AccordionTrigger>
    <AccordionContent>
      Yes. It adheres to the WAI-ARIA design pattern.
    </AccordionContent>
  </AccordionItem>
</Accordion>;
```

### Example: Icons

```tsx
import { Icon } from "@/components/ui/icon";
import { ArrowRight } from "lucide-react-native";

<Icon as={ArrowRight} className="text-foreground" size={16} />;
```

## 📂 Project Structure

- `app/`: File-based routing (Expo Router).
- `components/ui/`: Reusable UI components (shadcn style).
- `lib/`: Utilities and theme configurations.
- `global.css`: Global styles and CSS variables for theming.
- `tailwind.config.js`: Tailwind configuration with custom colors and animations.

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License.
