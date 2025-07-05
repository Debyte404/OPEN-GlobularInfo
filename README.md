# 🌍 GlobularInfo

**GlobularInfo** is a one-stop itinerary generator for spontaneous travel planning. Whether you're exploring your hometown or venturing abroad, GlobularInfo pulls rich insights from public APIs to craft personalized journeys in real time.

---

## 🚀 Features Tackled

### 🟢 Easy (2 points each)

- **Creative 404/Error Handling:**  
  Thoughtful fallback experience with a custom-designed error page that keeps the vibe alive even when things break.

- **Dark Mode Support:**  
  Seamless support based on system or user preference for visual comfort across time zones and screen types.

- **Custom Loading States:**  
  Engaging weather-aware spinners and animated loaders while waiting on backend or API data.

---

### 🔵 Medium (4 points each)

- **Dynamic Theming Based on API Data:**  
  Real-time styling shifts based on current weather, using API-driven visual transformations to create immersive UI changes.

---

### 🔴 Hard (6 points each)

- **Voice Navigation & Accessibility Enhancements:**  
  Control buttons via speech (e.g., “generate”, “facts”), and colorblind-friendly themes elevate inclusivity and ease of use.

- **Text-to-Speech for Content:**  
  Paragraphs are readable aloud via Web Speech API for multitaskers, commuters, and visually impaired users.

---

## 🧠 APIs Used

- [🔮 Gemini Flash 2.5](https://ai.google.dev/)
- [🧰 API NINJAS Suite](https://api-ninjas.com/)
  - Weather API  
  - Reverse Geocoding  
  - Historical Events  
- [🎮 PokéAPI](https://pokeapi.co/)  
  (For assigning Pokémon based on regional traits)

---

## 🛠️ Setup Instructions

### 🔌 Backend

- Add keys to `.env`:

```env
API_NINJAS_KEY=xxxx
GEMINI_API_KEY=xxxx
```

- CORS Setup (inside `index.js`):

```js
app.use(cors({ origin: "https://globular-info.vercel.app" }));
```

> Replace the origin above with your own frontend domain.

---

### 🎨 Frontend

- In `config.js`:

```js
export var backendAPI = "http://localhost:5000/api";
```

> Swap out with your production backend domain.

---

## 🧭 Flow Overview

1. 🔔 On load, frontend sends a wake-up ping to backend  
2. 📍 Requests location permission and fetches GPS coordinates  
3. 🌐 Maps location to a rotating Earth using **Three.js**  
4. 🏠 Converts lat/lng to readable address (region, state, country)  
5. 🌦️ Queries live weather and updates UI dynamically  
6. 🧳 Generates full itinerary with:
    - 3 regional foods  
    - 3 must-see destinations  
    - 3 key local phrases  
    - 1 contextual Pokémon (for fun + context)
7. 📚 Fetches historical facts about the place you're in

---

## ♿ Accessibility Features

- 📣 Text-to-Speech support for reading content aloud  
- 🗣️ Voice commands: say `"generate"` or `"facts"` to trigger actions  
- 🌓 Dark mode + responsive UI for mobile/tablet  

---

## 📱 UI Highlights

- Fully responsive and mobile-friendly  
- Reactivity based on weather and location  
- Interactive globe visualization with smooth transitions
- custom 404 page

---

![Screenshot_6-7-2025_42534_globular-info vercel app](https://github.com/user-attachments/assets/4eb30f86-8059-41ab-905f-39b87f04fa88)

![Screenshot_6-7-2025_42153_globular-info vercel app](https://github.com/user-attachments/assets/07aa6d88-6424-493c-b129-ff1208c2e18c)

![Screenshot_6-7-2025_4251_globular-info vercel app](https://github.com/user-attachments/assets/bbc9a809-f2af-46ce-b203-9dc49398c701)

## ✨ Project Status

GlobularInfo is actively maintained and evolving. Ideas like adding route optimization, social sharing, or multilingual support are in the pipeline — stay tuned!

---

## 👤 Author

Made by [Ankit](https://github.com/yourprofile)  
Built with curiosity, creativity, and caffeine ☕ for Call2Code 2025
```
