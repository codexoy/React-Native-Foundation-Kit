# React Native Foundation Kit

**Enterprise-Ready Starter Template for React Native Applications**

Version: 3.2.0 | React Native: 0.72.0 | License: MIT

## Overview

React Native Foundation Kit is a comprehensive starter template designed to accelerate your mobile app development. This production-ready foundation includes essential features, best practices, and scalable architecture patterns to kickstart your next React Native project.

## Quick Start

### Installation & Setup

```bash
# Clone the repository
git clone https://github.com/codexoy/react-native-foundation.git
cd react-native-foundation

# Install dependencies
yarn install

# iOS setup
cd ios && pod install && cd ..

# Rename project (optional)
npx react-native-rename "YourAppName"

# Start development
yarn start
```

### Platform-Specific Launch

```bash
# Android
yarn android

# iOS
yarn ios

# Both platforms
yarn mobile
```

## Project Architecture

```
src/
├── components/          # Reusable UI components
├── screens/            # App screens and pages
├── navigation/         # Routing configuration
├── store/              # State management
├── services/           # API and external services
├── utils/              # Helper functions
├── constants/          # App constants and configs
├── assets/             # Images, fonts, icons
├── themes/             # Design system and styling
└── locales/            # Internationalization files
```

## Core Features

### Built-In Functionality
- Modern Navigation: React Navigation v6 with stack, drawer, and bottom tabs
- UI Framework: React Native Paper with Material Design components
- Theming System: Light/Dark theme support with easy customization
- Multi-Language: i18n support with English and Persian (easily extendable)
- Typography: Custom font system with multiple weight support
- Image Management: Advanced image picking and optimization
- Splash Screen: Customizable launch screen

### Developer Experience
- TypeScript Ready: Full type safety configuration
- Code Quality: ESLint, Prettier, and pre-commit hooks
- Testing Setup: Jest and React Native Testing Library
- Debugging Tools: Reactotron and Flipper integration
- VS Code Config: Optimized editor settings

## Design System

### Theme Configuration
```javascript
const theme = {
  colors: {
    primary: '#6366F1',
    secondary: '#EC4899',
    background: '#FFFFFF',
    surface: '#F8FAFC',
    error: '#EF4444',
    text: '#1F2937',
  },
  spacing: {
    xs: 4,
    sm: 8,
    md: 16,
    lg: 24,
    xl: 32,
  },
  typography: {
    fontFamily: {
      regular: 'Inter-Regular',
      medium: 'Inter-Medium',
      bold: 'Inter-Bold',
    }
  }
}
```

## Configuration

### Environment Setup
```bash
# Copy environment template
cp .env.example .env

# Configure environment variables
API_URL=https://api.yourservice.com
APP_ENV=development
```

### Customization Guide
1. Update app name in app.json and package.json
2. Modify theme colors in src/themes/
3. Add your brand assets to src/assets/
4. Configure navigation structure in src/navigation/
5. Set up API endpoints in src/services/

## Available Scripts

```bash
# Development
yarn start          # Start Metro bundler
yarn android        # Run on Android
yarn ios            # Run on iOS

# Testing
yarn test           # Run unit tests
yarn test:watch     # Run tests in watch mode
yarn lint           # Run ESLint
yarn type-check     # Run TypeScript compiler

# Building
yarn build:android  # Build Android APK
yarn build:ios      # Build iOS archive
```

## Testing & Quality

### Test Structure
```bash
# Unit tests
yarn test

# Coverage report
yarn test:coverage

# E2E tests (if configured)
yarn test:e2e
```

### Code Quality Tools
- ESLint: JavaScript/TypeScript linting
- Prettier: Code formatting
- Husky: Git hooks for pre-commit validation
- Commitlint: Conventional commit messages

## Internationalization

Add new languages easily:
```javascript
// src/locales/spanish.json
{
  "welcome": "Bienvenido",
  "login": "Iniciar Sesión"
}
```

## Deployment

### Android
```bash
# Generate release APK
cd android && ./gradlew assembleRelease

# Or bundle for Play Store
./gradlew bundleRelease
```

### iOS
```bash
# Archive for App Store
cd ios && xcodebuild -workspace App.xcworkspace -scheme App -configuration Release archive
```

