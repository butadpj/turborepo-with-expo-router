## Steps taken after starting the project with `npx create-turbo@latest -e with-react-native-web`

- Select `yarn workspace` (it could be whatever you want)
- Update expo version to `~49.0.7`. Re-install dependencies again from the project's root
- Run `sudo npx expo install --check`, then fix the dependencies

- At this point, the project can be successfuly run without any errors. We can now proceed and add `expo-router` 👇

---

### Used this [expo-router docs](https://docs.expo.dev/routing/installation/#quick-start) as a guide

- Run `npx expo install expo-router react-native-safe-area-context react-native-screens expo-linking expo-constants expo-status-bar react-native-gesture-handler`
- Run `yarn install` from project's root
- Remove `index.js`'s content and replace it with `import "expo-router/entry";`. See [working with monorepos guide](https://docs.expo.dev/guides/monorepos/)
- Set `"scheme": "turborepo-with-expo-router"` in `app.json` (Replace the schema with whatever you like)
- Add `plugins: ["expo-router/babel"],` in `babel.config.js`
- Create `.env` file and add `EXPO_USE_METRO_WORKSPACE_ROOT=1`
- Finally, remove `App.tsx` and start creating the first page in `/app`
