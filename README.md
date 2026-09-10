# Paradise Nursery 🌿

**Paradise Nursery** is an e-plantShopping React + Redux shopping cart web application for an online plant shop. It lets customers browse houseplants organized into categories, add them to a shopping cart, and manage the quantities of items in their cart before checkout.

This is the final project for the IBM/Coursera **"Developing Front-End Apps with React"** course.

## Live Demo

🔗 Deployed app: `https:aqeeloffsec.github.io/e-plantShopping/`

## Project Overview

Paradise Nursery consists of three main views:

1. **Landing Page** – A welcome page with a background image, the company name ("Paradise Nursery"), a short paragraph about the company, and a **Get Started** button that leads to the product listing page.
2. **Product Listing Page** – Displays houseplants grouped into multiple categories (Air Purifying, Aromatic Fragrant, Insect Repellent, Medicinal, and Low Maintenance Plants). Each plant card shows a thumbnail image, name, description, price, and an **Add to Cart** button. The header/navbar includes a shopping cart icon that dynamically displays the total number of items in the cart, plus navigation links to the Home, Plants, and Cart views.
3. **Shopping Cart Page** – Lists every plant type currently in the cart with its thumbnail, unit price, quantity, and line total. Each item has **increase (+)** and **decrease (-)** quantity buttons and a **Delete** button. The page prominently displays the total number of plants and the total cost of the cart, along with **Continue Shopping** and **Checkout** buttons.

## Features

- 🌱 Six+ unique houseplants across five categories
- 🛒 Add to Cart with an instantly disabled button once a plant has been added
- 🔢 Cart icon badge in the header that updates in real time
- ➕➖ Increase / decrease quantity controls in the cart
- 🗑️ Delete individual plant types from the cart
- 💵 Live-calculated per-item and cart-wide totals
- ↩️ Continue Shopping button to return to the product listing
- ✅ Checkout button (displays a "Coming Soon" message)
- 📱 Responsive layout for mobile and desktop
- 🗃️ State managed globally with Redux Toolkit (`CartSlice.jsx`)

## Tech Stack

- [React](https://react.dev/) (Vite)
- [Redux Toolkit](https://redux-toolkit.js.org/) + [React Redux](https://react-redux.js.org/)
- CSS3 (no external UI framework)
- [GitHub Pages](https://pages.github.com/) for deployment

## Project Structure

```
e-plantShopping/
├── src/
│   ├── App.jsx           # Landing page + top-level view switching
│   ├── App.css           # Landing page styling (incl. background image)
│   ├── AboutUs.jsx        # "About the company" content shown on the landing page
│   ├── AboutUs.css
│   ├── ProductList.jsx    # Product listing page, navbar, cart icon
│   ├── ProductList.css
│   ├── CartItem.jsx       # Shopping cart page
│   ├── CartItem.css
│   ├── CartSlice.jsx      # Redux slice: addItem, removeItem, updateQuantity
│   ├── store.js           # Redux store configuration
│   └── main.jsx           # App entry point / Redux Provider
├── index.html
├── package.json
└── vite.config.js
```

## Getting Started Locally

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later recommended)
- npm

### Installation

```bash
git clone https://github.com/aqeeloffsec/e-plantShopping.git
cd e-plantShopping
npm install
```

### Run the development server

```bash
npm run dev
```

The app will be available at `http://localhost:5173`.

### Build for production

```bash
npm run build
```

## Deployment (GitHub Pages)

This project uses the [`gh-pages`](https://www.npmjs.com/package/gh-pages) package.

1. Update the `homepage` field in `package.json` and the `base` field in `vite.config.js` with your GitHub username/repo name.
2. Run:

```bash
npm run deploy
```

3. In your GitHub repository settings, set the GitHub Pages source branch to `gh-pages`.

## Author

Built as part of the IBM Front-End Development course capstone project.

## License

This project is provided for educational purposes.
