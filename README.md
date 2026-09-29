# Pokédex

A React-based Pokédex application that lets users browse the original 151 Pokémon, search by name or Pokédex number, view Pokémon details, and explore their moves and sprites.

## Features

* Browse all 151 original Pokémon
* Search Pokémon by:

  * Name
  * Pokédex number
* Select a Pokémon from the navigation panel
* Display Pokémon:

  * Name
  * Pokédex number
  * Types
  * Base stats
  * Sprites
  * Moves
* Click on a move to view its description
* Cache Pokémon and move data using `localStorage`
* Fetch Pokémon and move information from the PokéAPI
* Responsive interface

## Built With

* React
* JavaScript
* Vite
* CSS
* PokéAPI
* Browser `localStorage`

## How It Works

The application uses the PokéAPI to retrieve Pokémon data.

When a Pokémon is selected, its Pokédex number is used to construct an API request:

```text
https://pokeapi.co/api/v2/pokemon/{id}
```

The returned data is stored in React state and displayed throughout the application.

Move data is handled separately. Each Pokémon's move information contains a URL pointing to the corresponding move resource in the PokéAPI. When a move is clicked, that URL is fetched to retrieve the move description.

The application also uses `localStorage` to cache previously fetched Pokémon and move data, reducing unnecessary API requests.

## Search

The search functionality filters the original 151 Pokémon based on the user's input.

Users can search using either:

```text
Pokédex number
```

or:

```text
Pokémon name
```

For example:

```text
025
```

or:

```text
Pikachu
```

## Project Structure

```text
src/
├── components/
│   ├── Modal.jsx
│   ├── PokeCard.jsx
│   ├── SideNav.jsx
│   └── TypeCard.jsx
│
├── utils/
│   └── index.js
│
├── App.jsx
└── main.jsx

public/
└── pokemon/
    ├── 001.png
    ├── 002.png
    └── ...
    └── 151.png
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Wayne-Bowen/Pok-dex.git
```

Navigate into the project:

```bash
cd Pok-dex
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Then open the local URL provided by Vite in your browser.

## What I Learned

This project helped me practice:

* React components
* Props
* `useState`
* `useEffect`
* Conditional rendering
* Array methods such as `map()`, `filter()`, and `find()`
* Event handling
* API requests with `fetch()`
* Working with nested API responses
* Dynamic object property access
* `localStorage`
* JSON parsing and stringifying
* Search and filtering
* Rendering data dynamically in React

## API

This project uses [PokéAPI](https://pokeapi.co/) to retrieve Pokémon and move data.

## Author

**Wayne Bowen**

Junior Frontend Developer

GitHub: [Wayne-Bowen](https://github.com/Wayne-Bowen)
