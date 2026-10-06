### For using pwa installation and setup

- can follow this link : https://medium.com/@dlrnjstjs/building-a-react-pwa-creating-a-web-app-that-feels-native-57bd21ec03e5

- install `npm install vite-plugin-pwa -D`

- in vite.config.js edit this 
    VitePWA({
      registerType: 'autoUpdate',  // Automatically update Service Worker
      includeAssets: ['favicon.ico', 'robots.txt', 'apple-touch-icon.png'],  // Files to cache
      manifest: {
        name: 'My First PWA',  // Full app name
        short_name: 'PWA App',  // Short name displayed on home screen
        description: 'My first Progressive Web App built with React',
        theme_color: '#ffffff',  // Color of the top bar
        background_color: '#ffffff',  // Splash screen background color
        display: 'standalone',  // Makes it look like a native app (hides browser UI)
        icons: [
          {
            src: 'pwa-192x192.png',  // Small icon
            sizes: '192x192',
            type: 'image/png'
          },
          {
            src: 'pwa-512x512.png',  // Large icon
            sizes: '512x512',
            type: 'image/png',
            purpose: 'any maskable'  // Works in various environments
          }
        ]
      }
    })

- after this npm run build not npm run dev to buld .manifest and server files, after this 
React + Vite + Tailwind
          +
     PWA plugin
          ↓
manifest
service worker
Workbox
app icons

we are here 

