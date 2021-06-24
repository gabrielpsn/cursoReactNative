# cursoReactNative

Bibliotecas para meu App reac-native


npm install styled-components
npm install @react-navigation/native
npm install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view

apos instalar o react importar no index.js o react-native-gesture-handler

npm install @react-navigation/stack
npm install @react-navigation/bottom-tabs
npm install @react-native-community/async-storage
npm install @react-native-community/geolocation
npm install @react-native-permissions


Configurar o android
android/app/src/main
androidManifest

adicionar linha user-permission = android.permission.ACCESS_FINE_LOCATION
para dar permissao de localização

npm install react-native-swiper
npm install react-native-svg
npm install react-native-svg-transformer

abrir arquivo metro.config.js

colar codigo da biblioteca

const { getDefaultConfig } = require("metro-config");

module.exports = (async () => {
  const {
    resolver: { sourceExts, assetExts }
  } = await getDefaultConfig();
  return {
    transformer: {
      babelTransformerPath: require.resolve("react-native-svg-transformer")
    },
    resolver: {
      assetExts: assetExts.filter(ext => ext !== "svg"),
      sourceExts: [...sourceExts, "svg"]
    }
  };
})();


depois adicionar getTransformer
