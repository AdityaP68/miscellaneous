#### Pre ES-module era code

- needed to import all the js files into the main html form the to be loaded and be in scope for them to share there scope, and the order of the file import also matters, basically its the same thing as a variable being used before actually being declared.

1. Dependency Management:

- In the pre-ES modules era, managing dependencies between different JavaScript files was manual and error-prone. Developers had to carefully order script tags in HTML to satisfy dependencies.

2. Global Scope and Namespace Pollution:

The lack of a native module system led to the use of patterns like IIFE and namespacing to avoid polluting the global namespace. However, these patterns had limitations and could become unwieldy in large projects.

3. Script Loading Overhead:

Loading multiple script files individually resulted in additional HTTP requests, leading to slower page load times, especially for larger applications.

A bundler addresses all these challenges and provides several key features, (ex.  webpack, esbuild, parcel, vite, etc.)

An overlook of webpack

Module Bundling:

1. Webpack bundles modules and their dependencies into a single or multiple output files. This bundling process allows developers to structure their code using modern module systems (such as ES modules or CommonJS) and still deliver a single optimized file to the browser.
Loaders:

2. Webpack supports loaders, which are transformations applied to source code files. This enables Webpack to process various types of files, including transpiling modern JavaScript (e.g., using Babel), handling stylesheets, and more.
Code Splitting:

3. Webpack supports code splitting, allowing developers to split their code into smaller chunks. This is particularly useful for optimizing the initial load time of an application by loading only the essential code upfront.
Asset Management:

4. Webpack manages assets like images, fonts, and other resources. It can optimize and bundle these assets as part of the build process.
Plugin System:

5. Webpack has a powerful plugin system that provides additional functionality. Plugins can perform tasks such as code minification, environment-specific configuration, and more.