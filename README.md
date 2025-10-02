# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.

---

## Styling and UI setup in this repo

This project is preconfigured with:

- NativeWind (Tailwind for React Native) with CSS variables and dark mode
- tailwindcss-animate for utility animations
- Path aliases via `@/*`
- Portal host for overlays
- shadcn-style config and a reusable Accordion component
- `lucide-react-native` icon wrapper with `className` support

### What was added

- Tailwind config: `tailwind.config.js` (colors from CSS variables, dark mode, animations, hairline width)
- Global CSS tokens: `global.css` (light/dark `:root` variables)
- Portal host: added to `app/_layout.tsx`
- Theme tokens and React Navigation theme: `lib/theme.ts`
- Classname merge helper: `lib/utils.ts` (`cn`)
- shadcn config: `components.json`
- UI components scaffold: `components/ui/accordion.tsx`, `components/ui/icon.tsx`

### Quick start

1) Install deps (already done in this repo, for reference):

```bash
npx expo install nativewind tailwindcss tailwindcss-animate
npx expo install lucide-react-native react-native-svg
npm i class-variance-authority clsx tailwind-merge @rn-primitives/portal
```

2) Start the app:

```bash
npx expo start
```

### Using the icon wrapper

```tsx
import { Icon } from '@/components/ui/icon';
import { ArrowRight } from 'lucide-react-native';

<Icon as={ArrowRight} className="text-foreground" size={16} />
```

### Using the Accordion

```tsx
import { Accordion, AccordionItem, AccordionTrigger, AccordionContent } from '@/components/ui/accordion';

<Accordion type="single" collapsible>
  <AccordionItem value="item-1">
    <AccordionTrigger>Section</AccordionTrigger>
    <AccordionContent>Content</AccordionContent>
  </AccordionItem>
  {/* ... */}
</Accordion>
```

### Notes

- Dark mode is class-based (`dark`) and colors map to CSS variables in `global.css`.
- The `PortalHost` is mounted in `app/_layout.tsx` for modals/overlays.
- Path aliases like `@/components` and `@/lib` are configured in `tsconfig.json`.
