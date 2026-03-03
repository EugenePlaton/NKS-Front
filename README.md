# NKS Frontend (React E-commerce Showcase)

A frontend web application for a laboratory furniture manufacturer/distributor, built as an e-commerce style catalog with filtering, product cards, cart interactions, and contact pages.

This project solves a practical business need: presenting a product assortment online, helping customers discover items faster through filters, and enabling a simple “add to cart” flow before checkout or manager contact.

It is aimed at:
- Manufacturing and B2B furniture teams that need a modern product showcase
- Frontend developers looking for a real-world React + Bootstrap storefront example
- Employers/clients who want to evaluate practical UI integration with REST APIs

## Tech Stack

- **React 17**
- **React Router DOM 6**
- **React Bootstrap + Bootstrap**
- **react-use-cart** (cart state)
- **react-yandex-maps** + Yandex Maps embed
- **Create React App** build toolchain

## Key Features

- Dynamic catalog rendering from backend API endpoints (`products`, `table`, `contacts`, etc.)
- Product filtering UI with selectable filter variants and checkbox options
- Cart interaction (add items, item counter, clear cart action)
- Contact and company pages with phone/email links and map embed
- Responsive storefront layout with reusable components and preloaded assets

## Project Structure

```text
src/
  components/
    products/
      filters/
  pages/
  css/
public/
  assets/
```

## Quick Start

### 1) Prerequisites
- Node.js 16+ (recommended)
- npm 8+

### 2) Install dependencies
```bash
npm install
```

### 3) Configure environment variables
Create a `.env.local` file in the project root and define API-related values used in the code:

```env
REACT_APP_NKS_API=http://localhost:8000/
REACT_APP_NKS_PHOTO_PRODUCTS_PATH=http://localhost:8000/media/
```

> `REACT_APP_NKS_API` is used in multiple data-fetching components, and `REACT_APP_NKS_PHOTO_PRODUCTS_PATH` is used for product images.

### 4) Run in development mode
```bash
npm start
```
Open [http://localhost:3000](http://localhost:3000).

### 5) Build for production
```bash
npm run build
```

### 6) Optional: serve built files with Node/Express
```bash
node nks_build.js
```
This serves the production build on port `9000`.

## Live Demo

No public demo URL is currently configured in the repository.

If you deploy it (e.g., Vercel/Netlify/Nginx), add your link here.

## API Expectations

The frontend expects a backend with endpoints similar to:
- `GET /products`
- `GET /products/filtersAll`
- `GET /products/filter?...`
- `GET /table`
- `GET /product`
- `GET /contacts`
- `GET /contact`

## Available Scripts

In the project directory, you can run:

### `npm start`
Runs the app in development mode.

### `npm test`
Launches the test runner in interactive watch mode.

### `npm run build`
Builds the app for production to the `build` folder.

### `npm run eject`
**Note: this is a one-way operation.**

## Create React App Notes (kept from original template)

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

Useful references:
- [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started)
- [React documentation](https://reactjs.org/)
- [Code Splitting](https://facebook.github.io/create-react-app/docs/code-splitting)
- [Analyzing the Bundle Size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)
- [Making a Progressive Web App](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)
- [Advanced Configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)
- [Deployment](https://facebook.github.io/create-react-app/docs/deployment)
- [Troubleshooting build minification](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
