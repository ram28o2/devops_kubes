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
  * Updates results instantly as the user types

* **Filter by Type**

  * Filter Pokémon based on type (Fire, Water, Grass, etc.)
  * Types are dynamically fetched from the API

* **Pagination**

  * Navigate through Pokémon using next/previous controls
  * Efficient client-side pagination

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
  * Graceful error message handling

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
* **Styling:** Plain CSS (beginner-friendly, no frameworks)
* **API:** PokéAPI

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
git clone <your-repo-url>
cd pokedex-lite
```

---

### 2. Install dependencies

```bash
npm install
```

---

### 3. Run the application

```bash
npm start
```

---

### 4. Open in browser

```
http://localhost:3000
```

---

# 🌐 API Used

* [https://pokeapi.co/](https://pokeapi.co/)

---

# 🔹 Bonus Features

## ✨ Animations

* Subtle animations added for better user experience:

  * Card hover effects
  * Button interactions
  * Modal transitions
  * Page transitions

---

## 🔐 OAuth Authentication (Separate Branch)

* A basic OAuth login flow is implemented as a proof-of-concept in a separate branch:

```
auth-oauth
```

### Includes:

* Google Login (working)
* GitHub Login (basic PoC using redirect flow)

### Purpose:

* Demonstrates understanding of OAuth authentication
* Not a full production implementation

---

## ⚡ Server-Side Rendering (SSR)

* SSR was explored conceptually using frameworks like Next.js

### Benefits:

* Faster initial page load
* Better SEO

### Status:

* Not implemented in the main project
* Can be added in a separate branch if needed

---

# ⚠️ Challenges Faced

* Handling large API data efficiently
* Managing pagination with filtering and search together
* Avoiding unnecessary API calls
* Maintaining smooth UI while fetching data

---

# 💡 Solutions

* Used client-side filtering after fetching data
* Implemented pagination using array slicing
* Used localStorage for persistence (favorites)
* Managed loading state carefully to avoid UI flicker

---

# 📌 Future Improvements

* Improve performance with caching
* Add backend for full OAuth authentication
* Enhance UI with better design system
* Add unit testing

---

# 🔗 Live Demo

👉 (Add your Vercel / Netlify link here)

---

# 📂 Repository

👉 (Add your GitHub repo link here)

---

# 🙌 Conclusion

This project focuses on building a clean, responsive, and user-friendly application while following good coding practices and scalable structure.

---
