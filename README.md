# React Native v0.71.1 : Expo Bare Workflow project

## Before start
1. Deberás tener corriendo nodeJS 16 por lo menos (proyecto ejecutado en `v16.14.2`).
2. Deberás [ver qué versión instalar](https://docs.gradle.org/current/userguide/compatibility.html) de Java deberás tener instalada vs la versión del gradle que tengas en el proyecto.
(Para ver qué version tienes, debes ir a `android\gradle\wrapper\gradle-wrapper.properties` y buscar el atributo `distributionUrl`)

## Corriendo proyecto
```bash
cd "D:\Documentos\react-native projects\WorkerMultithreadingSample"
npx react-native run-android
npx react-native run-ios
```

## Renombrando el proyecto
<!-- See https://medium.com/the-react-native-log/how-to-rename-a-react-native-app-dafd92161c35. <br> -->
Si deseas renombrar todo el proyecto desde raíz, debes realizar los siguientes pasos:
1. Copy icons (if you changed it): (it will be replaced by defaults after)
- from iOS:
  - `ios/WorkerMultithreadingSample/Images.xcassets`
- from Android:
  - `android\app\src\main\res\drawable`
  - `android\app\src\main\res\mipmap-hdpi`
  - `android\app\src\main\res\mipmap-mdpi`
  - `android\app\src\main\res\mipmap-xhdpi`
  - `android\app\src\main\res\mipmap-xxhdpi`
  - `android\app\src\main\res\mipmap-xxxhdpi`
2. Update `displayName` and `name` in `app.json` to the new name
3. Delete `ios/` and `android/` directories
  - if you got some java.exe processes running in background, you can execute before deleting those folders:
  ```bash
  wmic process where "name like '%java%'" delete
  ```
4. Run `npx react-native eject` (install first using `npm i react-native-eject @react-native-community/cli`)
5. Replace the icons you copied earlier
<!-- 6. Run `npx react-native link` (only RN =< 0.69) (install first using `npm i react-native-link`) -->
 <!-- - If didn't work, please delete 'node_modules' and run 'yarn' in console. -->
6. Please reinstall [Install Bare Workflow Expo](#expo_section_bare_workflow)
6. Start your app and hope it worked! Or read the rest of this tutorial.

## How was installed?
1. Execute React Native create command: (https://reactnative.dev/docs/environment-setup)
```bash
# add '... --version 0.71.1' if you want a specific React Native project version.
npx react-native init MyAwesomeProject
```
### <a id="expo_section_bare_workflow"></a>Install Bare Workflow Expo:
1. Execute Automatic Installation to integrate Bare Workflow Expo: (see `https://docs.expo.dev/bare/installing-expo-modules/`)

```bash
# ignore ERROR:'pod-install' if you're on Windows / Linux.
npx install-expo-modules@latest
```

2. Probar si Expo funciona antes de echarle mano al código:

```bash
expo install expo-constants
```

```javascript
// App.tsx
import Constants from 'expo-constants';
console.log(Constants.systemFonts);
```