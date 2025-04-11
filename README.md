# React Carousel Component

![Preview](https://i.imgur.com/LjIu4y0.png)

This repository contains two implementations of a carousel component in React:
   - A custom-built carousel
   - A carousel using the `react-slick` library

## Figma URL of design

[Slider](https://www.figma.com/file/QfMzzThSYmgabSvn4t8Yfe/Slider?node-id=0%3A1&t=IpsYjMUn3Xj3Hs3N-1)

## Features

### Custom Carousel (`Carousel.jsx`)
- Manual implementation without external dependencies
- Smooth slide transitions using CSS transforms
- Auto-advancing slides (2 second interval)
- Previous/next navigation buttons
- Circular navigation (wraps around at ends)
- Responsive design

### Slick Carousel (`SlickCarousel.jsx`)
- Built using `react-slick` library
- Auto-play functionality
- Fade transition effect
- Pause on hover
- Navigation dots
- Responsive by default

## Installation

- Clone the repository:
   ```bash
   git clone https://github.com/Durubhuru14/react-carousel.git
   ```

- Install dependencies:
   ```bash
   cd react-carousel
   npm install
   ```

- Run the development server:
   ```bash
   npm run dev
   ```

## Usage

### Custom Carousel
```jsx
import Carousel from './Carousel';

function App() {
  return (
    <div>
      <Carousel />
    </div>
  );
}
```

### Slick Carousel
```jsx
import SlickCarousel from './SlickCarousel';

function App() {
  return (
    <div>
      <SlickCarousel />
    </div>
  );
}
```

## Data Structure
The carousels use data from `data.js` which contains:
- `shortList`: Single item (for testing)
- `list`: 4 items (default)
- `longList`: 8 items (for extended testing)

Each item has:
- `id`: Unique identifier
- `image`: URL of the person's image
- `name`: Person's name
- `title`: Person's title/position
- `quote`: Testimonial quote

## Dependencies
- React
- react-icons (for navigation icons)
- react-slick (for SlickCarousel)
- slick-carousel (styles for SlickCarousel)

## Styling
All styles are in `index.css` using CSS variables for consistent theming.

## Switching Between Carousels
In `App.jsx`, you can comment/uncomment the carousel components to switch between implementations:
```jsx
// To use custom carousel:
<Carousel />

// To use slick carousel:
<SlickCarousel />
```