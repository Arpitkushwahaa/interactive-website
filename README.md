# Spectral - Interactive 3D Visuals

A modern, interactive 3D visualization website built with React, Three.js, and Framer Motion. This project showcases various 3D objects with different interaction modes including rotation, zoom, and particle effects.

## Features

- Interactive 3D models with multiple visualization modes
- Smooth animations and transitions using Framer Motion
- Stunning visual effects including particles, color transitions, and dynamic UI elements
- Responsive design that works on all device sizes
- Dark/light mode toggle

## Technologies Used

- React with TypeScript
- Three.js and React Three Fiber for 3D rendering
- Framer Motion for animations
- Tailwind CSS for styling
- Vite for fast development and building

## Development

To run the project locally:

```bash
# Install dependencies
npm install

# Start the development server
npm run dev
```

## Deployment

### Deploy to Netlify

This project is configured for easy deployment to Netlify:

1. Create a Netlify account at [netlify.com](https://www.netlify.com/)
2. Click "Add new site" > "Import an existing project"
3. Connect to your Git provider (GitHub, GitLab, Bitbucket)
4. Select your repository
5. Netlify will automatically detect build settings from the netlify.toml file
6. Click "Deploy site"

Alternatively, you can deploy directly from your local machine:

```bash
# Install Netlify CLI
npm install netlify-cli -g

# Login to your Netlify account
netlify login

# Initialize and deploy
netlify init
netlify deploy --prod
```

### Deploy to GitHub Pages

If you prefer GitHub Pages, you can use:

```bash
# Build and deploy the project
npm run deploy
```

## Project Structure

- `src/components/three/` - Contains 3D scene and interactive canvas components
- `src/components/sections/` - Main content sections of the website
- `src/components/layout/` - Layout components like header and footer

## License

MIT License 