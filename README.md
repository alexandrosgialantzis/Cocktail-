# CocktailDB

# Introduction
A React app for finding cocktails. You type in the search box, the app asks TheCocktailDB for matching drinks and shows them as cards. Click a card to see the full recipe.

# Features
1. Live search that runs on every key you press.
2. Cards with a photo, the name, the glass and whether the drink has alcohol.
3. A page for each drink with the category, the ingredients and the steps.
4. An error page for any address the app does not know.

# Technologies
React, React Router, Create React App, plain CSS.

# Installation
1. Clone the repository.
2. Install dependencies with npm install.
3. Start the app with npm start.

# How it works
The search term, the list of drinks and the loading flag all live in one place, src/context.js. The provider watches the search term and calls the API again whenever it changes. It also renames the long API fields into short ones, so the rest of the app works with id, name and image.

The search form pushes what you type into that shared state. The list reads the same state and picks one of three things to show: the spinner, a short message when nothing matched, or the grid of cards. The single drink page is on its own and fetches by the id it reads from the address.

#Structure
src/context.js holds the shared state. src/pages has the four screens. src/components has the search form, the list, the card and the loader. public/_redirects keeps deeper addresses working after a reload.
