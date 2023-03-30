---
sidebar_position: 1
---

# Folder Structure

```bash
.
├── /android/                   # android-specific code (bootstrapped from `react-native init`)
├── /ios/                       # ios-specific code (bootstrapped from `react-native init`)
├── /node_modules/              # 3rd-party libraries and utilities
├── /jest/                      # Configurations for unit testing
├── /src                        # Javascript or typescript code
|   /assets                     # **Optional** if you'd like to keep them outside of your components
│       ├── /fonts/
│       ├── /images/
│       └── /videos/
|   /HOC                        # Commonly used higher order components
|   /config                     # App configurations
|   /Constants                  # App constants
|   /Enums                      # Enums for routes, slices etc
|   /Components                 # Basic components for the entire application, each component have respective folders and it includes the files below
│       ├── Foo.component.tsx   # Component file
│       ├── Foo.test.js         # Unit testing
│       └── Foo.style.ts        # style file
|   /Hooks                      # Commonly used hooks
|   /Interface                  # Interfaces for routes, slices, components etc
|   /Screen                     # App screens, each screen have respective folders and it includes the files below
│       ├── Foo.screen.tsx      # Screen file
│       ├── Foo.style.tsx       # Style file
│       └── /Partials/          # Components for the screen
|   /Redux                      # Redux Store
|   /Routes                     # **Optional** if you'd like to keep them outside of your components
│       ├── Navigation Hook
│       ├── Pages
│       ├── RootNavigation
│       └── Tab Navigation
|   /Services                   # This folder contains services that related to api calls and backend
│       ├── API                 # All the API calls from the app
│       └── Requests            # Axios configurations
|   /Styles                     # **Optional** Global Styles
|   /Utils                      # **Optional** Utility functions
|   /Webview                    # **Optional** Contains html files and configurations for webview
└── package.json                # The list of 3rd party libraries and utilities
```
