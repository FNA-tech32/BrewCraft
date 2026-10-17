<div align="center">

# BrewCraft

A coffee shop storefront for browsing drinks and meals, placing orders, and managing the shop.

BrewCraft sells good meals and especially coffee, with high quality beans, healthy meals, and drinks made for a better start to the day.

</div>

## Overview

This is the front end for BrewCraft. Customers can explore the menu, add items to a cart, and check out. Signed-in customers can manage a profile and review past orders. Admins can track sales, manage products and promos, and mark orders as done.

The app is a Create React App project. Menu, account, and order data come from a REST API set in the environment.

## What the site includes

**Home**

- Hero: “Start Your Day with Coofee and Good Meals”
- Store figures: 90+ staff, 800+ customers, 30+ stores
- What the shop provides: high quality beans, customizable healthy meals, staff chat while ordering, and a free member card from IDR 200.000
- Featured drink: Hazelnut Latte (IDR 25.000)
- Store map, partner logos, and customer reviews
- Promo call to action

**Menu and ordering**

- Product catalog with search, sort, and category filters
- Categories: Favorite & Promo, Coffee, Non Coffee, Foods, and Add-on
- Product detail with size options (Regular, Large, Xtra Large)
- Cart with delivery address, phone number, notes, and payment
- Order history and order detail

**Account**

- Register, login, forgot password, and reset password
- Profile, including photo and password updates
- Logout

**Admin**

- Sales dashboard with daily, weekly, and monthly reports
- Create and edit products
- Create and edit promos
- Manage orders and mark them done

## Pages

| Path | Who can open it | What it does |
| --- | --- | --- |
| `/` | Anyone | Home page |
| `/products` | Anyone | Menu, search, sort, and promos |
| `/products/category/:id` | Anyone | Menu filtered by category |
| `/products/detail/:productId` | Anyone | Product detail |
| `/cart` | Anyone | Cart and checkout |
| `/auth/login` | Guests | Sign in |
| `/auth/register` | Guests | Create an account |
| `/auth/forgotpass` | Guests | Request a password reset |
| `/auth/resetpass` | Guests | Set a new password |
| `/profile` | Signed-in users | Profile |
| `/history` | Signed-in users | Order history |
| `/history/:id` | Signed-in users | One order |
| `/admin` | Admins | Sales reports |
| `/manage-order` | Admins | Incoming orders |
| `/products/new` | Admins | Add a product |
| `/products/edit/:productId` | Admins | Edit a product |
| `/promo/new` | Admins | Add a promo |
| `/promo/edit/:promoId` | Admins | Edit a promo |

## Tech stack

- [React](https://react.dev/) 18 and [React Router](https://reactrouter.com/)
- [Redux Toolkit](https://redux-toolkit.js.org/) and [Redux Persist](https://github.com/rt2zz/redux-persist) (cart and session in local storage)
- [Axios](https://axios-http.com/) for the API
- [Tailwind CSS](https://tailwindcss.com/) and [DaisyUI](https://daisyui.com/)
- [React Hot Toast](https://react-hot-toast.com/) for notifications
- [Victory](https://commerce.nearform.com/open-source/victory/) for admin charts
- [Day.js](https://day.js.org/) for dates
- [react-image-crop](https://github.com/DominicTobias/react-image-crop) for profile photos

## Getting started

### Prerequisites

- [Node.js](https://nodejs.org/) 14 or newer (LTS recommended)
- A BrewCraft REST API. Product, auth, cart checkout, history, and admin screens call this host.

### Installation

1. Install dependencies:

   ```bash
   npm install
   ```

2. Create a `.env` file in the project root:

   ```env
   REACT_APP_BACKEND_HOST=http://localhost:8080
   REACT_APP_WEBSITE_NAME=BrewCraft
   ```

   `REACT_APP_BACKEND_HOST` is the API base URL. `REACT_APP_WEBSITE_NAME` is used in the browser tab title and the persisted Redux key.

3. Start the app:

   ```bash
   npm start
   ```

   The site opens at [http://localhost:3000](http://localhost:3000).

### Other scripts

| Command | Purpose |
| --- | --- |
| `npm start` | Development server |
| `npm run build` | Production build in `build/` |
| `npm test` | Run tests |

## Contact

- Email: hello@brewcraft.example
- Phone: +1 (555) 014-2840
- Address: 42 Harbor Lane, Portland, OR 97201

## License

This project is licensed under the ISC License. See [LICENSE](LICENSE).
