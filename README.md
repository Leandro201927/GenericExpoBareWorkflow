# React Native v0.71.1 : Expo Bare Workflow project

## Before start
1. Deberás tener corriendo NodeJS v16 o v18 por lo menos.
2. Deberás ver qué versión de Java deberás tener instalada vs la versión del gradle que tengas en el proyecto.
(Para ver qué version tienes, debes ir a 'android\gradle\wrapper\gradle-wrapper.properties' y buscar el atributo 'distributionUrl')
[Ver matriz de compatibilidad](https://docs.gradle.org/current/userguide/compatibility.html)

## How was installed?

```bash
# add '... --version 0.68.0' if you want a specific React Native project version.
npx react-native init MyAwesomeProject

```
### Install Bare Workflow Expo:
2. Execute Automatic Installation to integrate Bare Workflow Expo: (see `https://docs.expo.dev/bare/installing-expo-modules/`)

```bash
# ignore 'pod-install' error if you're on Windows / Linux.
npx install-expo-modules@latest
```

3. Probar si Expo funciona antes de echarle mano al código:

```bash
expo install expo-constants
```

```javascript
// App.tsx
import Constants from 'expo-constants';
console.log(Constants.systemFonts);
```