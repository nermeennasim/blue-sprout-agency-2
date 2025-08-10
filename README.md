<<<<<<< HEAD
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      ...tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      ...tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      ...tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

# 📧 Email Testing Documentation - Blue Sprout Agency

## 📋 Quick Overview

This documentation provides comprehensive testing procedures for the Blue Sprout Agency contact form email system using Resend API.

**System Overview:**
- **Frontend**: React contact form
- **Backend**: Node.js + Express API
- **Email Service**: Resend API with verified domain
- **Business Email**: `support@bluesproutagency.com`

## 🚀 Pre-Testing Checklist

Before testing, ensure the following are configured:

### ✅ Environment Setup
```bash
# Check your .env file contains:
NODE_ENV=development
PORT=3001
RESEND_API_KEY=your_actual_resend_api_key_here
```

### ✅ Domain Verification
- [ ] `bluesproutagency.com` is verified in Resend dashboard
- [ ] DNS records are properly configured
- [ ] `support@bluesproutagency.com` can receive emails

### ✅ Server Status
```bash
# Start your backend server
cd backend
npm run dev

# Verify server is running
curl http://localhost:3001/health
```

Expected response:
```json
{
  "status": "OK",
  "timestamp": "2025-08-09T...",
  "port": 3001,
  "envLoaded": true
}
```

## 🧪 Testing Procedures

### Test 1: Configuration Verification

**Purpose**: Verify email service is properly configured

```bash
curl http://localhost:3001/api/test
```

**Expected Response:**
```json
{
  "message": "Email routes are working",
  "timestamp": "2025-08-09T...",
  "configuration": {
    "configured": true,
    "hasApiKey": true,
    "businessEmail": "support@bluesproutagency.com",
    "businessName": "Blue Sprout

=======
# blue-sprout-agency-2
This is Business Website of my Own Blue Sprout Agency
>>>>>>> c5e8a44fbdd2cab2948e6c0cdf19a05adad5fe19


