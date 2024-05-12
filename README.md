# React Folder Structure

Welcome to the open-sourced file and folder structure for React applications! This repository provides a comprehensive and organized layout for structuring your React projects, aimed at improving maintainability, scalability, and collaboration among developers.

```
src/
├── assets/
│   ├── images/
│   │   ├── logo.png
│   │   └── background.jpg
│   ├── icons/
│   │   ├── icon.svg
│   │   └── arrow.png
│   └── fonts/
│       ├── Roboto-Regular.ttf
│       └── FontAwesome.otf
├── components/
│   ├── Button/
│   │   ├── Button.js
│   │   └── Button.css
│   ├── Navbar/
│   │   ├── Navbar.js
│   │   └── Navbar.css
│   └── Modal/
│       ├── Modal.js
│       └── Modal.css
├── config/
│   ├── env/
│   │   ├── .env.development
│   │   └── .env.production
│   ├── constants.js
│   └── index.js
├── contexts/
│   ├── ThemeContext/
│   │   └── ThemeContext.js
│   └── AuthContext/
│       └── AuthContext.js
├── hooks/
│   ├── useLocalStorage/
│   │   └── useLocalStorage.js
│   └── useFetch/
│       └── useFetch.js
├── pages/
│   ├── Home/
│   │   └── Home.js
│   ├── Profile/
│   │   └── Profile.js
│   └── Dashboard/
│       └── Dashboard.js
├── services/
│   ├── api/
│   │   ├── userService.js
│   │   └── postService.js
│   ├── auth.js
│   └── axios.js
├── styles/
│   ├── theme/
│   │   ├── lightTheme.js
│   │   └── darkTheme.js
│   └── global.css
├── utils/
│   ├── format/
│   │   └── format.js
│   ├── validate/
│   │   └── validate.js
│   └── helpers/
│       ├── stringHelpers.js
│       └── dateHelpers.js
├── lib/
│   ├── apiClient.js
│   ├── constants.js
│   ├── logger.js
│   └── themeUtils.js
├── store/
│   ├── actions/
│   │   ├── userActions.js
│   │   └── postActions.js
│   ├── reducers/
│   │   ├── userReducer.js
│   │   └── postReducer.js
│   ├── selectors/
│   │   ├── userSelectors.js
│   │   └── postSelectors.js
│   └── index.js
├── routes/
│   ├── routes.js
│   └── PrivateRoute.js
└── types/
    ├── interfaces/
    │   ├── User.ts
    │   └── Post.ts
    └── enums/
        ├── Status.ts
        └── Role.ts
```

## Overview

Managing the architecture of a React application can be challenging as projects grow in complexity. This repository offers a standardized structure that promotes modularity, reusability, and clarity in code organization.

## Features

- Modularization: Components, services, utilities, and other functionalities are organized into separate directories, promoting encapsulation and reusability.
- Scalability: The structure accommodates the growth of your project, making it easier to add new features or modules without cluttering the codebase.
- Consistency: By following a standardized structure, developers can maintain consistency across different parts of the application, improving readability and maintainability.
- Extensibility: The structure is designed to be flexible and adaptable, allowing you to customize and extend it based on your project's specific requirements.

## Contents

This repository includes the following directories:

- **assets**: Contains static assets such as images, icons, and fonts used in the application.
- **components**: Houses reusable UI components used throughout the application.
- **config**: Stores configuration files, constants, or settings used across the application.
- **contexts**: Contains context providers for managing global state using React Context API.
- **hooks**: Holds custom hooks for sharing logic between components.
- **pages**: Contains routed components representing different pages or views in the application.
- **services**: Houses abstractions for making API requests or other external services.
- **styles**: Contains shared styles or theme-related files used throughout the application.
- **utils**: Holds utility functions or helper modules used across the application.
- **lib**: Contains third-party libraries initialization used across the application.
- **store**: Houses Redux-related files such as action types, reducers, selectors, and the main Redux store configuration.
- **routes**: Contains route configuration files or constants defining the routes used in the application.
- **types**: Holds TypeScript type definitions used throughout the application.

## Additional Information

You can enable absolute path in your project setup using the following options:

1. **Vite**:
   
In Vite, configure the `alias` option in your `vite.config.js` file to set up aliases for absolute paths.

```
import { defineConfig } from 'vite';
import path from 'path';

export default defineConfig({
  resolve: {
    alias: {
      '@': path.resolve(__dirname, 'src'),
    },
  },
});
```

2. **Create React App (CRA)**:

In Create React App, add a `jsconfig.json` or `tsconfig.json` file in the root of your project, and configure the `baseUrl` and `paths` options to set up aliases for absolute paths.

```
{
  "compilerOptions": {
    "baseUrl": "src",
    "paths": {
      "@/*": ["*"]
    }
  }
}
```

Enabling absolute paths in your project setup offers several advantages, primarily aimed at improving code maintainability and developer experience. One key reason is to avoid the need for cumbersome relative path chaining (e.g., `../../../`) in import statements.

```
// Without absolute path
import Button from '../../../../components/Button';

// With absolute path
import Button from '@/components/Button';
```

## Conclusion

Adopting this folder structure enhances React project organization, boosting productivity and collaboration. It offers modularity, scalability, and consistency, streamlining development and improving the developer experience. We encourage its use and welcome contributions. 

Thank you for considering this approach. Happy coding!
