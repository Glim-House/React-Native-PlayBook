---
sidebar_position: 4
---

# Navigations

## Types of Navigation

- Stack Navigation
- Tab Navigation
- Drawer Navigation

## Nested Navigation

Nesting navigation means rendering a navigator inside of screen of another navigator. for example: Tab Navigation inside the screen of a Stack navigation

```js
function Home() {
  return (
    <Tab.Navigator>
      <Tab.Screen name="Feed" component={Feed} />
      <Tab.Screen name="Messages" component={Messages} />
    </Tab.Navigator>
  );
}

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen
          name="Home"
          component={Home}
          options={{ headerShown: false }}
        />
        <Stack.Screen name="Profile" component={Profile} />
        <Stack.Screen name="Settings" component={Settings} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
```

> Note: In a typical React Native app, the NavigationContainer should be only used once in your app at the root. You shouldn't nest multiple NavigationContainers unless you have a specific use case for them.

## Best Practices

- Always create seperate files for navigation. Don't include naviagtion inside the `App.tsx`.
- Use **Enum** for route names. Don't hard code.

## References

- [https://reactnavigation.org/](https://reactnavigation.org/)
