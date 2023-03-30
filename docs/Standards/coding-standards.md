---
sidebar_position: 2
---

# Coding Standards

Writing code may easy, but well-structured one is powerful! The code should also be *Reliable, Scalable, and Maintainable*. 


- Your app should contain a proper `README.md` file that explains your app. Clearly mention the features, functionalities, contributions guidelines, installation process, guide, etc.
- Organize Imports: Sorting imports is a good practice, divide each imports such as: 
    - React Imports
    - Library Imports
    - Absolute imports from the project
    - Relative Imports
- Follow [Folder Structure](../codebase/folder-structure.md) and [Naming Conventions](./naming-standards.md)
- Keep the component and screen clean, have a look at [component structure](../codebase/component-structure.md)
- Keep the app responsive and avoid Inline Styling
  - use `<SafeAreaView>` component is used to ensure that the content of your app is displayed correctly and not overlapped by the device's status bar or rounded corners.
  - Inline styling is more difficult to maintain if there is any change in style, you have top change 100 lines of code. Instead of inline style you have to define styles with unique class names in stylesheet.
- Document everything 
  - Write comments that are legal, informative, explanatory of intent, and offer clarification.
- Remove logs
- Always Handle Errors
  - It’s important to handle errors that occur in your application, whether they are caused by problems with your code or by external factors like network issues or API errors.We use try catch blocks to handle exceptions inside the app.
 - Use a linter to make your code easier to review.