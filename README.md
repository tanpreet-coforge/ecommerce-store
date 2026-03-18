# StorePro - E-Commerce Monolith

A modern, fully-featured e-commerce application built with Next.js, React, TypeScript, and Tailwind CSS. Features a responsive design, product search, shopping cart, and mock checkout system.

## Features

### 🛍️ Product Catalog
- **12 Pre-loaded Products** with detailed information
- **High-Quality Product Images** from Unsplash
- **Dynamic Product Grid** with responsive layout
- **Product Ratings & Reviews** system
- **Category Tags** for better organization
- **Stock Status Display** with inventory tracking

### 🔍 Advanced Search & Filtering
- **Full-Text Search** across product names, descriptions, and tags
- **Category Filtering** (Electronics, Sports, Travel, Furniture, Home)
- **Real-time Search Results** with instant loading
- **Mobile-Friendly Filter Panel** with toggle display
- **Price Range Information** display

### 📦 Shopping Cart
- **Add to Cart Functionality** with quantity selection
- **Cart Item Management** (increase, decrease, remove)
- **Real-time Cart Updates** with persistent storage (localStorage)
- **Cart Badge** showing total items
- **Order Summary** with subtotal, tax, and shipping calculations
- **Free Shipping** on orders over $100
- **Dynamic Total Calculation** (8% tax, $10 flat shipping or free)

### 💳 Mock Checkout
- **Complete Checkout Form** with validation
- **Shipping Address Form** (Name, Email, Phone, Address, City, State, ZIP)
- **Payment Information Form** (Card Number, Expiry, CVV)
- **Auto-Formatting** for card number and expiry date
- **Order Confirmation** with unique order number
- **Animated Order Success** screen

### 🎨 Beautiful & Responsive UI
- **Modern Design** with Tailwind CSS
- **Gradient Headers** and themed sections
- **Smooth Animations** and transitions
- **Mobile-First Approach** with breakpoints for all screen sizes
- **Dark-Friendly Interface** with high contrast
- **Loading Skeletons** for better UX
- **Icon System** using Lucide React

### 📱 Responsive Design
- **Mobile (xs)**: Full-width, stacked layout
- **Tablet (md)**: 2-column grid for products
- **Desktop (lg)**: 3-column grid with sidebar filters
- **XL (xl)**: Optimized spacing and typography

### 🔐 Data Management
- **Mock Product Database** with realistic data
- **API Routes** for product fetching and filtering
- **Client-Side State Management** with React Context
- **LocalStorage Integration** for cart persistence
- **TypeScript** for type safety

## Tech Stack

- **Frontend Framework**: Next.js 16.1.7 with App Router
- **UI Library**: React 19.2.3
- **Styling**: Tailwind CSS 4 with PostCSS
- **Language**: TypeScript 5
- **Icons**: Lucide React 0.577.0
- **State Management**: React Context API
- **Build Tool**: Turbopack

## Project Structure

```
src/
├── app/                          # Next.js App Router pages
│   ├── api/
│   │   └── products/            # API routes for products
│   │       ├── route.ts         # Get all/filtered products
│   │       └── [id]/route.ts    # Get single product
│   ├── product/
│   │   └── [id]/page.tsx        # Product detail page
│   ├── cart/
│   │   └── page.tsx             # Shopping cart page
│   ├── checkout/
│   │   └── page.tsx             # Checkout page
│   ├── layout.tsx               # Root layout with providers
│   ├── page.tsx                 # Home/listing page
│   └── globals.css              # Global styles
├── components/                   # Reusable React components
│   ├── Navbar.tsx               # Navigation bar
│   ├── ProductCard.tsx          # Product card component
│   ├── Filters.tsx              # Category filters
│   └── CartItemComponent.tsx    # Cart item component
├── context/
│   └── CartContext.tsx          # Cart state management
├── lib/
│   └── products.ts              # Mock product data
└── types/
    └── product.ts               # TypeScript interfaces
```

## Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn package manager

### Installation

1. Navigate to the project directory:
```bash
cd ecommerce-store
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm run dev
```

4. Open your browser and navigate to:
```
http://localhost:3000
```

## Available Scripts

```bash
# Development server
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Run ESLint
npm run lint
```

## Features in Detail

### Search Functionality
- Enter search queries in the navbar search bar
- Search across product names, descriptions, and tags
- Results update instantly
- URL updates with search parameters for bookmarking

### Category Filtering
- Desktop: Sidebar filters on the left
- Mobile: Toggle filter panel
- Select a category to filter products
- "All Products" option to show everything

### Product Details Page
- Full product information with large image
- Detailed description and specifications
- Star rating system with review count
- Stock status with "Only X left" warning
- Quantity selector
- Add to cart from detail page
- Related products section (placeholder)

### Shopping Cart
- View all items in cart
- Modify quantities or remove items
- Real-time price calculations
- Tax and shipping calculations
- Free shipping threshold display
- Clear cart option
- Promo code field (placeholder for future)

### Checkout Process
1. Fill shipping information
2. Enter payment details
3. Review order summary
4. Submit order
5. See confirmation with order number

## Mock Data

The application includes 12 pre-loaded products across various categories:
- **Electronics**: Headphones, Camera, Smartwatch, Speaker, Mouse, Keyboard, Tablet
- **Sports**: Running Shoes, Yoga Mat
- **Travel**: Backpack
- **Furniture**: Office Chair
- **Home**: Coffee Maker

Each product includes:
- Product name and description
- Price with discount information
- Category classification
- Star rating (4.5-4.8)
- Number of reviews
- Stock quantity
- Product tags
- High-quality images from Unsplash

## State Management

### Cart Context
The cart is managed using React Context API with:
- Persistent storage using localStorage
- Methods: `addToCart`, `removeFromCart`, `updateQuantity`, `clearCart`
- Calculated values: `getTotalPrice()`, `getTotalItems()`
- Hydration-safe implementation for SSR

## Styling

### Tailwind CSS Configuration
- Custom color scheme with blue primary
- Responsive grid system (1/2/3 columns)
- Smooth transitions and animations
- Gradient backgrounds for hero sections
- Card-based design patterns

### Color Scheme
- **Primary**: Blue (#3b82f6)
- **Success**: Green (#22c55e)
- **Warning**: Orange (#f97316)
- **Danger**: Red (#ef4444)
- **Background**: Light gray (#f9fafb)

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Features

- Image optimization with Next.js Image component
- Code splitting with dynamic imports
- Lazy loading for images
- Skeleton loading states
- Optimized CSS with Tailwind JIT
- Fast refresh development experience

## Future Enhancements

- [ ] User authentication and profiles
- [ ] Order history and tracking
- [ ] Wishlist functionality
- [ ] Product reviews system
- [ ] Advanced filtering (price range, rating)
- [ ] Coupon/discount codes
- [ ] Multiple payment methods
- [ ] Inventory management
- [ ] Admin dashboard
- [ ] Email notifications

## Notes

- This is a **mock e-commerce store** for demonstration purposes
- Payment processing is simulated (2-second delay)
- All product data is stored in memory (no database)
- Cart data persists only in localStorage per browser/device
- No real payment transactions occur

## License

MIT License - Feel free to use this project for learning and development purposes.

## Support

For issues or questions, please check the code comments or create new issues in the repository.

---

**Happy Shopping! 🛒**

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
