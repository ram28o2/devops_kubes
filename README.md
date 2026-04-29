---

# 🧩 Pokedex Lite

A responsive web application that allows users to explore Pokémon data using the public PokéAPI.
Users can search, filter, paginate, mark favorites, and view detailed information about each Pokémon.

---

# 🚀 Features

## 🔹 Core Features

* **Pokémon Listing**

  * Displays Pokémon in a responsive grid layout
  * Shows name, image, and ID

* **Search**

  * Search Pokémon by name
  * Filters results in real-time as the user types

* **Filter by Type**

  * Filter Pokémon based on type (Fire, Water, Grass, etc.)
  * Types are dynamically fetched from the API

* **Pagination**

  * Navigate through Pokémon using next/previous controls
  * Pagination is handled on the client side using array slicing

* **Favorites**

  * Mark/unmark Pokémon as favorites
  * Favorites are stored in **localStorage**
  * Data persists after page refresh

* **Detail View (Modal)**

  * Click on a Pokémon to view detailed information
  * Includes stats and abilities
  * Smooth open/close interaction

* **Loading & Error Handling**

  * Loading spinner while fetching data
  * Basic error handling for API failures

---

# 🎨 UI & Responsiveness

* Fully responsive (mobile, tablet, desktop)
* Clean and simple layout
* CSS-based animations:

  * Card hover effects
  * Button interactions
  * Modal transitions
  * Page fade-in effect

---

# 🧠 Tech Stack

* **Frontend:** React (JavaScript)
* **HTTP Client:** Axios
* **State Management:** React Hooks (useState, useEffect)
* **Styling:** Plain CSS
* **API:** PokéAPI

---

# ⚡ Performance Considerations
* Limited the number of Pokémon fetched per request to avoid long loading times
* Used parallel API calls (Promise.all) to improve data fetching speed
* Avoided unnecessary re-renders by managing state updates carefully

---

# 📁 Project Structure

```
src/
 ├── components/
 │   ├── PokemonCard.jsx
 │   ├── SearchBar.jsx
 │   ├── TypeFilter.jsx
 │   ├── Pagination.jsx
 │   ├── Loader.jsx
 │   ├── PokemonModal.jsx
 │
 ├── pages/
 │   └── Home.jsx
 │
 ├── services/
 │   └── api.js
 │
 ├── styles/
 │   └── styles.css
```

---

# ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Ramprasanth7119/pokedex_lite.git
cd pokedex_lite
```

---

### 2. Install dependencies

```bash
npm install
```

---

### 3. Run the application

```bash
npm run dev
```

---

### 4. Open in browser

```
http://localhost:5173
```

---

# 🌐 API Used

* [https://pokeapi.co/](https://pokeapi.co/)

---

# 🔹 Bonus Features

## ✨ Animations

* Added simple CSS-based animations for better UX:

  * Card hover effect
  * Button interactions
  * Modal open transition
  * Page transition

---

## 🔐 OAuth Authentication (Separate Branch)

* Google OAuth login is implemented as a proof-of-concept in a separate branch:

```
auth-google
```

* This demonstrates basic integration of third-party authentication in the UI.
* It is a frontend-only implementation (no backend).

---

## ⚡ Server-Side Rendering (SSR)

* Explored SSR conceptually using frameworks like Next.js

### Benefits:

* Faster initial load
* Better SEO

### Status:

* Not implemented in this project

---

# ⚠️ Challenges Faced

* **Filtering only worked on the current page initially**

  * When pagination was added, filtering was applied only to the current page’s data
  * This caused cases where valid results existed but were not shown

* **Pagination + Filtering conflict**

  * Example: selecting a type on page 10 sometimes showed “No Pokémon found”
  * Even though matching Pokémon existed on other pages

* **Handling large API data**

  * Fetching detailed data (images, stats) for many Pokémon caused delays
  * Needed to balance performance vs usability

* **UI issues with small result sets**

  * When only one Pokémon was shown, the layout stretched awkwardly

---

# 💡 Solutions

* **Adjusted filtering approach**

  * Instead of relying only on paginated data, Updated the logic to reset pagination when filters change, ensuring users always see relevant results
  * Reset pagination when search/type changes to avoid empty states

* **Handled empty states properly**

  * Added clear message:

    * “No Pokémon found on this page”
  * This avoids confusion for users

* **Optimized data fetching**

  * Limited number of Pokémon fetched at once
  * Used `Promise.all` efficiently for parallel API calls

* **Improved UI behavior**

  * Fixed layout issues when fewer items are displayed
  * Ensured grid remains consistent

---

# 📌 Future Improvements

* Improve performance using caching or lazy loading
* Add backend support for full authentication
* Improve UI design and accessibility
* Add unit and integration testing

---

# 🔗 Live Demo

👉 Live Demo: https://pokedex-lite-xi.vercel.app/

---

# 📂 Repository

👉 Github Repo: https://github.com/Ramprasanth7119/pokedex_lite.git

---

# 🙌 Conclusion

This project focuses on building a clean and functional application while handling real-world issues like pagination, filtering, and API performance.

---
