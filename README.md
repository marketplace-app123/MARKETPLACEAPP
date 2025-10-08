# Marketplace (wrapper app)
App Expo semplicissima per mostrare categorie come icone e aprire il tuo sito dentro l'app (WebView).
- Tocca una categoria -> si apre l'URL in una WebView interna
- Tocca "Accedi/Registrati" -> apre l'URL di login del sito

## Avvio
```bash
npm install
npx expo start
```

## Configura le URL
Modifica `constants.ts` (LOGIN_URL, CATEGORIES[].url) con gli indirizzi reali del tuo sito/marketplace.

## Build per Store (EAS)
```bash
npm i -g eas-cli
eas login
eas build:configure
eas build -p android --profile preview
# (su Mac) eas build -p ios --profile preview
```

### Nota su policy Store
Apple a volte rifiuta app che sono solo un "sito in una WebView". Aggiungere piccole funzioni native (es. link deep, share, push) aumenta le chance di approvazione.
