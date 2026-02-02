# 🏢 NaviBuilding - Interactive Building Map Navigator

An interactive web application for navigating and exploring building floor maps. Allows users to search for rooms, view their location on interactive SVG floor plans, and get step-by-step navigation routes between floors.

## ✨ Features

- 🗺️ **Interactive Maps**: Visualize floors with interactive SVG rendering
- 🔍 **Advanced Search**: Search rooms by name, description, or category
- 📍 **Zoom & Pan**: Intuitive zoom and navigation controls on maps
- 🧭 **Multi-floor Navigation**: Get step-by-step directions between locations
- 📱 **Responsive Design**: Works seamlessly on desktop and mobile devices
- ⚡ **Optimized Performance**: Built with Next.js 15

## 🚀 Tech Stack

- **Framework**: [Next.js 15](https://nextjs.org)
- **React**: v19
- **Language**: TypeScript
- **State Management**: [Zustand](https://github.com/pmndrs/zustand)
- **Styling**: [Tailwind CSS](https://tailwindcss.com) v4
- **UI Components**: Custom components with [Radix UI](https://www.radix-ui.com)
- **Icons**: [Lucide React](https://lucide.dev)
- **Zoom/Pan**: [react-zoom-pan-pinch](https://github.com/BetterTyped/react-zoom-pan-pinch)

## 📦 Installation

### Prerequisites
- Node.js 18+
- npm, yarn, pnpm or bun

### Steps

```bash
# Clone the repository
git clone https://github.com/fallenxl/navibuilding.git
cd navibuilding

# Install dependencies
npm install

# Run development server
npm run dev

# Open in your browser
# http://localhost:3000
```

## 🏗️ Project Structure

```
src/
├── app/
│   ├── page.tsx           # Main page
│   ├── layout.tsx         # Root layout
│   └── globals.css        # Global styles
├── components/
│   ├── SVGRender.tsx      # SVG map renderer
│   ├── room-info.tsx      # Room information panel
│   ├── background.tsx     # Decorative background
│   └── ui/                # Reusable UI components
├── store/
│   └── room.store.ts      # Zustand global state
├── services/
│   └── room.ts            # Business logic services
├── lib/
│   └── utils.ts           # Utilities (cn for classes)
└── data/
    └── floors.json        # Floor and room data
```

## 🎯 Key Features

### Room Search
Search any room in real-time. Filter includes:
- Room name
- Room description
- Category (classroom, hallway, etc.)

### Interactive Visualization
- Zoom in/out with buttons or mouse wheel
- Auto-pan when selecting a room
- Touch controls for mobile devices

### Multi-floor Navigation
When you select a room:
1. Shows your current location
2. Displays step-by-step route
3. Indicates whether to go up or down floors

### Available Floors
- **Floor B1** - Basement (27 rooms)
- **Floor 1** - First floor (27 rooms)
- **Floor 2** - Second floor (31 rooms)
- **Floor 3** - Third floor (5 rooms)
- **Floor 4** - Fourth floor (1 room)

## 🎨 Design Features

- **Light/Dark Theme**: Automatic CSS variables support
- **Responsive Design**: Mobile-first approach
- **Smooth Animations**: Transitions between states
- **Accessible Components**: Built with Radix UI
- **Custom Background**: Decorative dot pattern

## 📱 Responsive Breakpoints

- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

## 🔧 Available Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm start        # Start production server
npm run lint     # Run linter
```

## 🚀 Deployment

### Vercel (Recommended)

```bash
npm install -g vercel
vercel
```

### Docker

```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```

## 📊 Global State Management

The project uses **Zustand** to manage:
- Available floors
- Selected floor
- Selected room
- Information panel state
- Search and selection methods

## 🎓 Key Learnings

- Efficient state management with Zustand
- Dynamic SVG rendering and interactivity
- Zoom/pan functionality with react-zoom-pan-pinch
- Reusable components with Tailwind CSS
- Type-safety with TypeScript

## 📝 License

MIT

## 👨‍💻 Author

Axl Santos

## 🤝 Contributing

Contributions are welcome! Please feel free to open an issue or submit a pull request.

---
