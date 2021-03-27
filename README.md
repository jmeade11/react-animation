# React Animation

## Project Set Up

1. Fork and clone this repository.
1. Change into the newly created directory with `cd react-animation`.
1. Install the dependencies with `npm i`.

### Create a Project from Scratch

If you'd like to start a new project _from scratch_ without cloning this repository, follow these steps instead:

1. Create a new react project using [create-react-app](https://create-react-app.dev/) by typing:
   ```sh
   npx create-react-app your-project-name
   ```
1. Install the additional dependencies with:
   ```sh
   npm i styled-components polished framer-motion react-router-dom
   ```
1. Create a theme and components directory inside of the src directory and add an index.js file to each. You can manually do this or do it at the command line by typing:
   ```sh
   mkdir src/theme src/components && touch src/theme/index.js src/components/index.js
   ```
1. Delete the `logo.svg`, `index.css`, and `App.css` files in the `src` directory.
   ```sh
   rm src/logo.svg src/index.css src/App.css
   ```
1. Open in your preferred code editor (type `code .` to open in Visual Studio Code).
1. In the `src/theme` directory create a file named `GlobalStyle.js`. If you're planning to follow along with the tutorial, make sure to copy the file contents from [`src/theme/GlobalStyle.js`](./src/theme/GlobalStyle.js) file in this repository into your file.

   ```js
   import { createGlobalStyle } from 'styled-components';

   const GlobalStyle = createGlobalStyle`
      /* GLOBAL STYLES HERE */
   
    `;

   export default GlobalStyle;
   ```

1. Inside the `src/theme/index.js` add the follow export:
   ```js
   export { default as GlobalStyle } from './GlobalStyle';
   ```
1. Replace the contents of `src/index.js` with the following:

   ```js
   import React from 'react';
   import ReactDOM from 'react-dom';
   import { BrowserRouter as Router } from 'react-router-dom';
   import { GlobalStyle } from './theme';
   import App from './App';

   ReactDOM.render(
     <React.StrictMode>
       <Router>
         <GlobalStyle />
         <App />
       </Router>
     </React.StrictMode>,
     document.getElementById('root')
   );
   ```

1. Replace the contents of `src/App.js` with:

   ```js
   const App = () => {
     return <h1>Hello World</h1>;
   };

   export default App;
   ```

1. Test your app using the npm start script (`npm run start`).
