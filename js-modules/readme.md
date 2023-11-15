## Pre-ES Module Era Code

Before ES6 module system was introduced, we needed to import all the js files into the main html form the to be loaded and be in scope for them to share there scope, and the order of the file import also matters, basically its the same thing as a variable being used before actually being declared.

Therefore bundlers came into picture and fulfilled this role, ex. Pebpack, Parcel, ESBuild, Vite, etc.

#### Code before introduction of any module system:
```html

<body>
    <script src="utils.js"></script>
    <script src="main.js"></script>
</body>

```

```js

// main.js
const result = add(5, 3);
console.log(result);

```

```js

// utils.js
function add(a, b) {
    return a + b;
}
  
```

#### Code under ES6 module system:
```html
<body>
  <!-- Use type="module" to indicate that this script is an ES module -->
  <script type="module" src="main.js"></script>
</body>
```

```js

// main.js
import { add } from './utils.js';

const result = add(5, 3);
console.log(result);

```

```js

// utils.js
export function add(a, b) {
  return a + b;
}

```

## Benefits of Module Bundlers

Module bundlers offer several benefits over the pre-ES module era:

- **Improved Dependency Management:** Manually handling dependencies between JavaScript files was error-prone and necessitated careful ordering of script tags in HTML. Module bundlers automatically resolve dependencies, eliminating the need for manual script tag ordering.

- **Reduced Namespace Pollution:** Lacking a native module system, developers relied on patterns like IIFE (Immediately Invoked Function Expression) and namespacing to prevent global namespace pollution. However, these approaches had limitations and became cumbersome in large projects. Module bundlers encapsulate code within modules, preventing global scope pollution and conflicts.

- **Optimized Code Delivery:** Loading numerous script files individually resulted in additional HTTP requests, leading to slower page load times, especially for larger applications. Module bundlers can optimize and bundle code, reducing HTTP requests and improving page load times.

- **Enhanced Development Workflow:** Module bundlers provide a streamlined development workflow, simplifying code organization and management.

## Webpack Overview

Webpack is a popular module bundler that offers several advantages:

- **Module Bundling:** Webpack consolidates modules and their dependencies into a single or multiple output files. This enables developers to utilize modern module systems (ES modules or CommonJS) while delivering a single optimized file to the browser.

- **Loaders:** Webpack supports loaders, which transform source code files. This allows Webpack to process various file types, including transpiling modern JavaScript (e.g., using Babel) and handling stylesheets.

- **Code Splitting:** Webpack supports code splitting, enabling developers to divide their code into smaller chunks. This optimization technique delays loading non-critical code until it's needed, improving initial page load times.

- **Asset Management:** Webpack manages assets like images, fonts, and other resources, optimizing and bundling them as part of the build process.

- **Plugin System:** Webpack's powerful plugin system extends its functionality. Plugins can perform tasks like code minification, environment-specific configuration, and more.


