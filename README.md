# ReactNotes

# Assignment 01: Inception

## What is Emmet ?

- Emmet is a toolkit for web developers that greatly enhances HTML and CSS coding productivity. 
- It allows you to write HTML and CSS code faster by using abbreviations and shortcuts that expand into well-formed code. 
- Originally known as Zen Coding, Emmet supports a wide range of integrated development environments (IDEs) and text editors.
- For example, typing `html:5` and hitting enter will generate a boilerplate code for HTML5.

## Difference between a Library and a framework ?

The terms "library" and "framework" are often used in the context of software development, and while they share some similarities, they have distinct differences:

1. **Control Flow:**
   - **Library:** A library is a collection of pre-written code that you can use in your program. It typically consists of functions, procedures, and classes that you can call to perform specific tasks. However, the overall control flow of your program remains in your hands.
   - **Framework:** A framework, on the other hand, provides a more structured architecture and dictates the flow of control in your application. In a framework, you often write code that fits into the framework's structure, and the framework manages the flow of control.

2. **Inversion of Control (IoC):**
   - **Library:** When using a library, you have more control over the flow of your application. Your code decides when and how to call the library functions.
   - **Framework:** Frameworks often follow the principle of Inversion of Control (IoC), meaning the framework controls the flow of the application. Your code is called by the framework at specific points rather than you explicitly calling the framework.

3. **Flexibility:**
   - **Library:** Libraries are generally more flexible since you can choose which components to use and how to integrate them into your application.
   - **Framework:** Frameworks provide a more opinionated structure, and while this can make development faster, it may also limit flexibility as you need to adhere to the framework's conventions.

4. **Size and Scope:**
   - **Library:** Libraries are typically smaller in scope and focus on specific tasks or functionalities. You can use multiple libraries together in a single project.
   - **Framework:** Frameworks are more comprehensive and provide a larger set of tools, often covering multiple aspects of application development, such as handling HTTP requests, database interactions, and more.

5. **Example:**
   - **Library:** jQuery is an example of a JavaScript library. It provides functions for tasks like DOM manipulation and AJAX requests.
   - **Framework:** Django (for Python) and Ruby on Rails are examples of web development frameworks. They include tools and conventions for building web applications.

In summary, while both libraries and frameworks are tools that help developers build applications more efficiently, the key distinction lies in the level of control and structure they impose on your code. 

**Libraries are more about providing reusable components, while frameworks provide a broader structure and dictate the flow of your application.**

## What is CDN , why do we use it ?

CDN stands for Content Delivery Network. 

It is a network of distributed servers strategically located across the globe to deliver web content, such as images, stylesheets, scripts, and other resources, to users more efficiently. 

The primary purpose of using a CDN is to improve the performance, reliability, and availability of web applications and websites.

Here are the key reasons why CDNs are used:

1. **Faster Content Delivery:**
   - CDNs reduce latency by serving content from servers that are geographically closer to the end-users. When a user requests a resource, the CDN delivers it from the nearest server, resulting in faster loading times.

2. **Load Distribution:**
   - CDNs distribute the load across multiple servers, preventing any single server from becoming overloaded with traffic. This helps to ensure consistent performance, especially during traffic spikes or heavy usage periods.

3. **Scalability:**
   - CDNs can scale easily to handle increased traffic and demand. This is important for websites and applications that experience varying levels of traffic throughout the day or during specific events.

4. **Reliability and Redundancy:**
   - CDNs provide redundancy and reliability by replicating content across multiple servers. If one server fails or experiences issues, the CDN can automatically reroute traffic to another available server, minimizing downtime.

5. **Bandwidth Savings:**
   - CDNs reduce the burden on the origin server by caching and delivering static content locally. This helps to save bandwidth on the origin server and reduces the overall server load.

6. **Security:**
   - CDNs often include security features, such as DDoS (Distributed Denial of Service) protection, SSL/TLS support, and other security measures. This helps to mitigate potential threats and enhance the overall security of web applications.

7. **Global Reach:**
   - With servers distributed worldwide, CDNs provide a global reach. This is particularly beneficial for websites and applications that cater to a global audience, ensuring that users from different regions experience fast and reliable access.

8. **Content Optimization:**
   - CDNs can optimize content for delivery, including compressing images, minifying scripts and stylesheets, and leveraging techniques like browser caching. This leads to improved performance and a better user experience.

Popular CDN providers include Akamai, Cloudflare, Amazon CloudFront, and others. Many websites and applications leverage CDNs to enhance their overall performance, reduce latency, and provide a more seamless experience for users regardless of their geographic location.

## Why is React known as react ?

React, a JavaScript library for building user interfaces, was developed by Facebook. It was open-sourced in 2013, and the name "React" reflects the library's primary focus on efficiently updating and rendering user interfaces in response to changes in data.

The name "React" implies the reactive nature of the framework, where the user interface reacts dynamically to changes in the application's state. React introduces a component-based architecture, allowing developers to build UIs by composing reusable and modular components. When the underlying data changes, React efficiently updates only the necessary components, which contributes to a more responsive and interactive user experience.

In summary, React is named for its emphasis on reactive programming, where the UI reacts to changes in the application state.

## What is cross origin in script tag ?

In web development, the same-origin policy is a security feature implemented by web browsers to prevent a web page from making requests to a different domain than the one that served the web page. This policy helps protect users from potential security threats, such as cross-site request forgery (CSRF) and cross-site scripting (XSS) attacks.

When you include a script tag in an HTML document to load an external script, such as a JavaScript file, the browser enforces the same-origin policy. If the script source (i.e., the URL specified in the `src` attribute of the script tag) is from a different origin (domain, protocol, or port) than the one that served the HTML page, the browser will block the script from being loaded. This restriction is known as a "cross-origin" or "cross-origin resource sharing" (CORS) limitation.

To handle cross-origin requests, the server should include appropriate CORS headers in its response to explicitly allow the browser to load and execute the script from a different origin. The CORS headers indicate which origins are permitted to access the resource and what types of requests are allowed.

Here's an example of how you might encounter a cross-origin issue in a script tag:

```html
<!-- This script tag will be blocked if the server doesn't include proper CORS headers -->
<script src="https://example.com/external-script.js"></script>
```

In the above example, if the script at "https://example.com/external-script.js" does not include the necessary CORS headers, the browser will block the script from loading due to cross-origin restrictions.

## What is the difference between react and react DOM ?

React and ReactDOM are two related but distinct packages in the React ecosystem:

1. **React:** Core React functionality
   - **Purpose:** The core React library is focused on providing the functionality for building user interfaces with a component-based architecture.
   - **Environment:** React can be used not only for web development but also for other platforms, such as mobile app development using React Native or virtual reality applications using React 360.
   - **Usage:** You write your components using React, which includes the virtual DOM, JSX syntax, and the core concepts like state and props.

2. **ReactDOM:** Manages DOM operations
   - **Purpose:** ReactDOM is a package specifically designed for web development. It provides the necessary tools to render React components in the browser.
   - **Environment:** ReactDOM is used in web applications to interact with the actual DOM (Document Object Model). It bridges the gap between the virtual DOM managed by React and the real DOM that the browser understands.
   - **Usage:** When you want to render a React component in a web page, you use ReactDOM. It includes methods like `ReactDOM.render()` to mount your React component into a specific HTML element in the DOM.

In summary, React is the core library for building user interfaces, and it is platform-agnostic. ReactDOM, on the other hand, is a package that specifically handles the interaction between React and the DOM when building web applications. If you're working on a web project, you'll typically use both React and ReactDOM together to create and render your UI components.

- What is the difference between react.development.js and react.production.js files via CDN ?

When you include React via a CDN (Content Delivery Network), you may notice that there are different versions of the library for development and production. The primary distinction between `react.development.js` and `react.production.js` lies in the optimizations applied to each version:

1. **react.development.js:**
   - **Development Version:**
     - Unminified and human-readable code.
     - Includes additional warnings and debugging information.
     - Larger file size, which aids in debugging and provides clearer error messages.
     - Suitable for development environments where debugging and detailed warnings are valuable.

   Example CDN link for development:
   ```html
   <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
   ```

2. **react.production.js:**
   - **Production Version:**
     - Minified and optimized for performance.
     - Warnings and debugging information are stripped out, resulting in a smaller file size.
     - Suitable for deployment in production environments where minimizing file size and optimizing performance are crucial.

   Example CDN link for production:
   ```html
   <script src="https://unpkg.com/react@17/umd/react.production.min.js"></script>
   ```

When deploying a React application to production, it is recommended to use the production version to reduce the size of the JavaScript bundle and improve the performance of your application. The development version, with its additional warnings and debugging features, is more appropriate for the development phase where you may need more information to identify and fix issues.

Remember to use the development version during development and switch to the production version for deployment to ensure optimal performance and a smaller payload for end-users.

## What is async and defer ?

- when we load a webpage 2 things happen: html parsing + loading of the script
- when loading of script tags happen: fetching the script + executing the script line by line
- **these are the 3 possible ways to write a script** : async | defer | using a script tag
1. **In normal Case**
   1. first the HTML Parsing begins.
   2. when a script tag is encountered the HTML parsing is stopped and the script fetching starts.
   3. After script fetching, the script execution takes place.
   4. After the script execution is finished, the HTML parsing starts again and continues.
   5. **Parsing -> fetch script -> execute script -> Parsing**
2. **In Aysnc Case**
   a. first the HTML Parsing begins.
   b. when a script tag is encountered the HTML parsing continues and the script fetching starts in parallel.
   c. After script fetching, HTML parsing is stopped and the script execution takes place.
   d. After the script execution is finished, the HTML parsing starts again and continues.
   e. **Parsing -> Parsing + fetch script -> execute script -> Parsing**
3. **In Defer Case**
   1. first the HTML Parsing begins
   2. when a script tag is encountered the HTML parsing continues and the script fetching starts in parallel.
   3. the script execution starts after the HTML parsing is completed.
   4. **Parsing -> Parsing + fetch script both complete -> execute script**
- Using an async attribues does not gaurantee the order of executing the scripts.
- If you want to use external script then we can use async script.

## What are arrow functions ?

Arrow functions do not bind their own `this` value. Instead, they inherit `this` from the enclosing scope. This behavior is different from traditional functions, which have their own `this` value.

```JS
function TraditionalFunction() {
    this.value = 1;

    setTimeout(function() {
        this.value++;
        console.log(this.value); // undefined (not what you might expect)
    }, 1000);
}

function ArrowFunction() {
    this.value = 1;

    setTimeout(() => {
        this.value++;
        console.log(this.value); // 2 (inherits `this` from the surrounding scope)
    }, 1000);
}

new TraditionalFunction(); // Logs "NaN"
new ArrowFunction();       // Logs "2"
```

# Episode 02: Igniting Our App

## Code in Episode 01

- The code written in Episode 01 is not optimized for production; it contains numerous comments and console logs.
- To address this, we need to implement code splitting, bundling, image optimization, and various other optimizations.
- In this episode, we will learn how to create our own production-ready create-react-app.

## Igniting the App

- React alone is insufficient for creating fast-running apps.
- There are many packages working behind the scenes to make the app fast and production-ready.

## NPM

- NPM does **NOT** stand for Node Package Manager but it is a package manager .
- NPM does not have a full form.
- NPM manages packages but does not stand for Node Package Manager.
- NPM is a package manager for JavaScript, serving as a standard repository for all packages.
- When we create a React app using create-react-app, it already includes NPM.

## Install NPM

- Use `npm init` to install it.
- If we do `npm init -y`, it skips a lot of steps.
- Once completed, it will prompt for various details, which we can fill accordingly.
    - Package name: (namaste-react)
    - Version: (1.0.0)
    - Description: This is the notes of Namaste React
    - Entry point: App.js
    - Test command: jest
    - Git repository: [https://github.com/RIBTAS007/namaste-react](https://github.com/RIBTAS007/namaste-react)
    - Keywords: react, JavaScript
    - Author: Satbir
    - License: ISC

- Upon hitting enter and submitting, we will obtain the [**package.json**](./episode-02-igniting-our-app/package.json), which is the configuration file for npm.

## Why Do We Need package.json

- Package.json is a configuration file.
- Our project depends on various packages, known as **dependencies**, and npm helps us manage them.
- NPM requires configurations like the version of the package, which are stored in package.json.

## Bundler

- The most crucial package for our project is a **bundler** like webapp, parcel, or vite.
- These bundlers help bundle and optimize our code for production.
- *They package our app properly so that it can be shipped to production.*
- Create React App uses **webapp** behind the scenes.
- In this episode, we will be using **Parcel** as our bundler.

## Parcel

- Use **npm install -D parcel** to install Parcel.
- It will fetch the Parcel packages from npm.
- The command to install anything is the same.
- `-D` in `install -D parcel` stands for installing it as a dev dependency.
- When we execute this command, it installs Parcel from npm.

## Types of Dependency:

- **Dev dependency**: Required in the development phase only.
- **Normal dependency**: Used in production also.

## After Parcel Installation

- Parcel will be mentioned as `"parcel": "^2.8.3"` in package.json as a dev dependency.
- The `^` symbol is used for version control; it automatically upgrades to the latest version. This is known as a caret.
- `~` is called a tilde, directly updating to the current major version available.

## package-lock.json

- We will now get another file, [**package-lock.json**](./episode-02-igniting-our-app/package-lock.json).
- **package-lock.json** tracks the exact dependencies installed, whereas **package.json** contains approximate versions.
- It also includes `integrity`, which contains a hash used to verify that the code on our dev machine and prod machine is the same.

## Node Modules

- **Node modules** contain all the code of dependencies fetched from npm.
- **Transitive dependencies**: We required Parcel, so we have the Parcel node module downloaded. This module has more dependencies, which further have more dependencies. Hence, all those dependencies are also downloaded in the node modules.
- Every node module has its own **package.json**, which stores details about its dependencies.
- We should not put our node modules on Git but should put package.json and package-lock.json, as they maintain the configurations of all the dependencies required. We can regenerate the node modules using `npm install`.
- **Whatever we can regenerate, don't put it on Git**. The lock in package-lock.json is there because it stores the exact versions used in our app.

## Ignite Our App

- Write `npx parcel index.html` where index.html is the source file of our project.
- Parcel will create a server for us, and our app will run at localhost.
- **npm** is for installing the packages.
- **npx** is for executing the packages.

## Installing React

- CDN links are not a good way to build React and React DOM in our project since it involves a costly operation for network calls. Also, if tomorrow the React version changes, it could pose a problem.
- Alternatively, we can install them as packages using `npm install react` and `npm i react-dom`.
- `npm i` and `npm install` are the same.
- We are not using -D here as we used during Parcel because we want it as a normal dependency, not as a dev dependency.
- Now we can remove the React CDN links from our **index.html**.
- When we write `import React from "react";`, it means we are referring to the React module installed and now present in our **node modules**.
- Also, update the script of calling app.js to `<script src="./App.js" type="module"></script>`; otherwise, we get the below error:
- **Browser scripts cannot have imports or exports**
- In index.html, we have app.js script, so it considers it a normal JS file or a browser script, and normal JS file does not have imports. So, we need to tell it that it is a module.
- Make sure to add `import React from "react";` and `import ReactDOM from "react-dom/client";` in app.js.

## What Does Parcel Do ?

- Dev build
- Local Server
- HMR = hot module replacement, (instantly refreshing the page on the browser)
- File watching Algorithm - written in C++ is used by Parcel to track the contents of the file.
- Caching - faster builds stored in **.parcel-cache**: Every time we build, the time reduces.
- Image optimization: load images in the browser
- Minification of the files
- Bundling of the files
- Compressing of the files
- Consistent hashing
- Code splitting
- Differential bundling - adjust code according to the browser, support older browsers.
- Diagnostics
- Error handling
- You can also host your app on https
- Tree shaking - remove unused code.
- Different dev and production bundles
- You can read the [Parcel Documentation](https://parceljs.org/)

## Creating a Production Build

- Use `npx parcel build index.html` to build the production build.
- This will give us an error, so we need to remove `main: "App.js"` from our package.json file.
- In the **dist** file, we will have the actual code after the production build.
- It will store the optimized code files.
- Browser list is an npm package that helps us manage which

 browsers we can use our app on.
- The parcel.cache and dist can be regenerated, so we don't need to put them on GitHub.

## Pushing to Git

- We push our code to Git, and the server fetches the code from Git. The server will host the app for the local user.
- We only need to push package and package-lock files.

## Make Our App Supported in Older Browsers

- For doing this, we need to know about browserslist, which is an npm package that we need to configure.
- In our package.json, we can add a key-value like `browserslist: []`, the value will be an array of browsers.
- We can check [browserlist.dev](https://browserlist.dev/) to know what we can add to the array.
- It does not mean it will not support other older browsers; it just means our app will surely support the browsers added to the array and may or may not support other versions.

## Summary

- React does not do everything.
- It's the job of the bundler. Here we have used **Parcel**.
- All this can be handled using **create-react-app**.

## Assignment 02

- [Click here](./Assignment02_IgnitingOurApp.md) for the assignment Questions and solutions

# Assignment 02: Igniting Our App

## What is NPM ?

NPM stands for Node Package Manager. It is a package manager for JavaScript programming language, primarily used for managing and sharing code packages for Node.js applications. NPM allows developers to easily install, publish, and manage dependencies and packages needed for their projects.

With NPM, developers can specify project dependencies in a `package.json` file, and NPM will automatically download and install those dependencies, along with their own dependencies, into the project's `node_modules` directory. This simplifies the process of managing dependencies and ensures that all collaborators on a project have access to the same versions of libraries and modules.

NPM also provides a command-line interface (CLI) for developers to execute various tasks such as installing packages, updating packages, running scripts defined in the `package.json` file, and more. Additionally, NPM hosts a public registry (npmjs.com) where developers can publish their own packages for others to use.

## What is Parcel/Webpack ? Why do we need it ?

Parcel and Webpack are both module bundlers for JavaScript applications, commonly used in front-end web development. They serve similar purposes but have different approaches and features.

1. **Parcel:**
   - Parcel is a "zero-configuration" module bundler, which means it requires minimal setup and configuration out of the box. It aims to simplify the build process for developers by automatically detecting dependencies and setting up an appropriate build pipeline.
   - Parcel supports various types of assets out of the box, including JavaScript, CSS, HTML, images, and more, without requiring additional configuration or plugins.
   - It provides built-in support for features like code splitting, hot module replacement (HMR), and tree shaking to optimize bundle size.
   - Parcel's simplicity and ease of use make it a popular choice for beginners or for projects where quick setup and minimal configuration are preferred.

2. **Webpack:**
   - Webpack is a highly configurable module bundler that offers a powerful and flexible build pipeline for JavaScript applications. It requires more configuration compared to Parcel but provides extensive customization options.
   - Webpack can handle not only JavaScript but also other assets like CSS, images, fonts, etc. through loaders and plugins, allowing for a wide range of customization and optimization options.
   - It supports advanced features such as code splitting, dynamic imports, tree shaking, and more, which are essential for optimizing performance and managing large-scale applications.
   - Webpack's ecosystem is extensive, with a large number of loaders and plugins available, allowing developers to tailor their build process to specific project requirements.

**Why do we need them?**
- **Module Bundling:** Both Parcel and Webpack help bundle various modules and assets into a single or multiple bundles that are optimized for deployment in the browser.
- **Dependency Management:** They manage dependencies efficiently, ensuring that all necessary files and modules are included in the bundle while optimizing the bundle size.
- **Optimization:** They optimize the bundle size by removing unused code (tree shaking), splitting code into smaller chunks (code splitting), and applying other optimization techniques to improve application performance.
- **Automation:** They automate repetitive tasks like transpiling code (e.g., from ES6 to ES5 using Babel), minification, and other build-related processes, saving developers time and effort.
- **Developer Experience:** Parcel and Webpack provide features like hot module replacement (HMR), which allows developers to see changes reflected instantly without needing a full page refresh, enhancing the development experience.
- **Compatibility:** They ensure compatibility with different browsers and environments by processing and transforming code and assets as needed.

In summary, Parcel and Webpack are essential tools for modern web development, providing efficient and optimized build processes, improving developer productivity, and ensuring high-performance applications. The choice between them depends on factors such as project requirements, developer preferences, and the level of customization needed.

## What is parcel-cache ?

Yes, when you build or run a React application using Parcel bundler, it does create a `.cache` folder by default. This `.cache` folder stores various caching data and intermediate build artifacts generated during the bundling process.

The purpose of this cache is to improve the build performance for subsequent builds. Parcel can reuse cached data from this folder, avoiding redundant processing of files that haven't changed since the last build. This can significantly speed up the build process, especially for larger projects with complex dependencies.

The `.cache` folder is typically automatically managed by Parcel, and users don't need to interact with it directly. However, in some cases, it can be useful to clear the cache manually, especially if you encounter build issues or want to ensure that the build process starts fresh.

## What is npx ?

`npx` is a package runner tool that comes bundled with npm (Node Package Manager) starting from npm version 5.2.0. It allows you to execute npm package binaries without having to install them globally or locally. The "npx" command can run any executable that's installed locally within a project or globally on your system.

Here are some key features and use cases of `npx`:

1. **Run packages without installation:** You can use `npx` to execute commands from packages that aren't installed on your system. For example, you can run `npx create-react-app my-app` to create a new React application without having to install `create-react-app` globally first.

2. **Execute specific versions:** `npx` allows you to specify a particular version of a package to use for a command. For instance, you can run `npx -p node@10 node --version` to execute the `node --version` command using Node.js version 10, even if a different version is installed globally on your system.

3. **Execute local binaries:** When working within a project directory, `npx` automatically looks for and runs binaries installed in the `node_modules/.bin` directory of that project. This allows you to run project-specific tools without having to reference their full path.

4. **Avoid global installs:** `npx` helps avoid cluttering your global npm packages by allowing you to run commands directly from packages without needing to install them globally. This can help keep your development environment clean and reduce potential conflicts between different versions of packages.

Overall, `npx` simplifies the process of running npm package binaries, especially for commands that you don't use frequently or that you only need for specific projects. It's a convenient tool for managing dependencies and executing commands in your development workflow.

## What is difference between dependencies and dev dependencies ?

In npm (Node Package Manager), dependencies and devDependencies serve different purposes and are typically specified in the `package.json` file of a Node.js project.

1. **Dependencies:**
   - Dependencies are packages that are required for the application to run in a production environment. These packages are necessary for the application's functionality.
   - When someone installs your package using npm (or when you install dependencies for your project), npm will automatically install all dependencies listed in the `dependencies` section of the `package.json` file.
   - Examples of dependencies include libraries, frameworks, utilities, or other packages that your application relies on for its core functionality during runtime.

2. **Dev Dependencies:**
   - DevDependencies are packages that are only needed during development and are not required for the application to run in a production environment.
   - When someone installs your package using npm, npm will not install devDependencies by default. These dependencies are typically used for development purposes only, such as testing, building, or debugging the application.
   - DevDependencies are useful for tools like testing frameworks (e.g., Jest, Mocha), build tools (e.g., webpack, Parcel), linters (e.g., ESLint, JSHint), and other utilities that assist with the development process but are not necessary for the deployed application to function.
   
In summary, dependencies are essential packages required for the application to run, while devDependencies are packages used for development purposes, such as testing and building, but are not necessary for the application's runtime execution. Separating dependencies and devDependencies helps keep the production environment clean and lean, as only the necessary runtime dependencies are installed.

## What is tree Shaking ?

Tree shaking is a term commonly used in the context of JavaScript module bundlers, such as Webpack, Rollup, and Parcel, to describe the process of eliminating dead or unused code from a bundle. The goal of tree shaking is to reduce the size of the final JavaScript bundle, thus improving the application's load time and performance.

Here's how tree shaking typically works:

1. **Static Analysis:** Tree shaking tools analyze the static code of the application, particularly the import and export statements used in ES6 modules. They build a dependency graph to determine which modules are imported and exported, and which functions, classes, or variables are used within those modules.

2. **Identifying Dead Code:** Once the dependency graph is constructed, the tree shaking tool identifies code that is not referenced or used anywhere in the application. This includes functions, classes, variables, or entire modules that are imported but never called or used.

3. **Elimination:** After identifying the dead or unused code, the tree shaking tool eliminates it from the final bundle. This process involves removing the code from the bundle entirely, ensuring that only the code necessary for the application's functionality remains.

By eliminating dead code, tree shaking helps optimize the size of the JavaScript bundle, resulting in smaller file sizes and faster load times for the application. This is particularly important for large applications with many dependencies, as it reduces the amount of unnecessary code that needs to be downloaded and parsed by the browser.

It's worth noting that tree shaking works best with ES6 module syntax (import/export) because it provides clear boundaries between modules, making it easier for the tool to determine unused code. Additionally, for tree shaking to be effective, the code must be written in a way that allows for static analysis, meaning that dynamic imports or other runtime-dependent code may not be optimized as effectively.

## What is Hot Module replacement ?

Hot Module Replacement (HMR) is a feature commonly found in modern JavaScript development tools like Webpack, Parcel, and others. It enables developers to update modules in an application without requiring a full page refresh, thus providing a faster and more efficient development experience.

Here's how Hot Module Replacement typically works:

1. **Detecting Changes:** When a developer makes changes to a file in their project, such as modifying a JavaScript module, a CSS file, or even a template file, the development server (e.g., webpack-dev-server) detects these changes.

2. **Module Replacement:** Instead of refreshing the entire page, the development server applies the changes only to the affected module or modules. It replaces the old module code with the updated code while keeping the application running in the browser.

3. **Preserving Application State:** HMR preserves the state of the application during module updates. This means that any data or application state that's currently displayed in the browser (such as form input values, UI state, etc.) remains unaffected by the module replacement.

4. **Instant Update in the Browser:** After applying the changes, the development server notifies the browser about the updated modules, and the browser reflects those changes instantly without reloading the entire page. This allows developers to see their changes reflected immediately without losing the current state of the application.

Hot Module Replacement greatly speeds up the development process by eliminating the need for manual page refreshes after making changes to the code. It provides a more seamless and interactive development experience, allowing developers to iterate quickly and see the impact of their changes in real-time.

HMR is especially valuable for front-end development, where developers often need to make frequent adjustments to styles, components, or application logic. It's widely used in conjunction with other development tools and workflows to enhance productivity and streamline the development process.

## List down 5 superpowers of parcel and describe any three of them in your own words

Parcel, a popular JavaScript module bundler, offers several powerful features that streamline the development workflow and enhance productivity. Here are five "superpowers" of Parcel:

1. **Zero Configuration:** Parcel requires minimal configuration to get started. It automatically detects and handles various file types (JavaScript, CSS, HTML, images, etc.) out of the box without requiring explicit configuration files. This simplicity reduces setup time and allows developers to focus more on writing code rather than configuring build tools.

2. **Fast Development Server:** Parcel comes with a built-in development server that offers fast rebuild times and hot module replacement (HMR) support. The development server automatically detects changes in the source code and updates the browser in real-time, providing a seamless development experience without manual page refreshes.

3. **Automatic Asset Optimization:** Parcel optimizes assets (such as images, CSS, and JavaScript) during the bundling process to improve performance and reduce file sizes. It automatically applies optimizations like minification, compression, and cache busting to ensure that the final bundle is optimized for production deployment.

4. **Efficient Code Splitting:** Parcel supports automatic code splitting, which allows developers to split their code into smaller chunks based on dynamic import statements or entry points. This feature helps reduce initial loading times by only loading the code that's needed for the current page, improving overall performance and user experience.

5. **Built-in Support for Modern Technologies:** Parcel has built-in support for modern JavaScript features (ES6+), CSS preprocessors (Sass, Less, Stylus), and bundling formats (CommonJS, ES modules). It seamlessly handles these technologies without additional configuration, making it easy to leverage the latest web development practices without worrying about compatibility issues.

Now, let's describe three of these superpowers in more detail:

1. **Zero Configuration:**
   - With Parcel's zero-configuration approach, developers can start building projects immediately without spending time on setup and configuration. This is particularly beneficial for beginners or small projects where simplicity and speed are priorities.
   - Developers don't need to create complex configuration files (such as webpack.config.js or babel.config.js) to define build settings or specify loaders and plugins. Parcel intelligently detects project dependencies and automatically applies appropriate transformations and optimizations.
   - By eliminating the need for manual configuration, Parcel reduces cognitive overhead and allows developers to focus on writing code rather than managing build tools.

2. **Fast Development Server:**
   - Parcel's built-in development server provides a fast and efficient environment for iterative development. It offers rapid rebuild times, allowing developers to see their changes reflected in the browser almost instantly.
   - The development server supports hot module replacement (HMR), which updates modules in the browser without reloading the entire page. This feature accelerates the development process by providing immediate feedback on code changes without disrupting the application state.
   - With Parcel's development server, developers can iterate quickly, experiment with different solutions, and debug issues in real-time, leading to a more productive and enjoyable development experience.

3. **Automatic Asset Optimization:**
   - Parcel automatically optimizes assets during the bundling process to improve performance and reduce load times. It applies optimizations such as minification, compression, and tree shaking to ensure that the final bundle is as small and efficient as possible.
   - By handling asset optimization automatically, Parcel simplifies the build process and eliminates the need for developers to manually configure and apply optimizations. This saves time and reduces the likelihood of human error.
   - Parcel's automatic asset optimization extends to various asset types, including JavaScript, CSS, images, fonts, and more. This comprehensive optimization ensures that the entire application bundle is optimized for optimal performance in production environments.

## What is '.gitignore'? What should we add and not add into it ?

`.gitignore` is a file used by Git to specify intentionally untracked files that Git should ignore. This file helps prevent irrelevant files, such as temporary files, build artifacts, or sensitive information, from being included in the version control system. By specifying patterns in `.gitignore`, developers can ensure that only relevant files are tracked and committed to the repository.

Here's what should be added to a `.gitignore` file:

1. **Build Artifacts:** Files generated during the build process, such as compiled binaries, minified JavaScript or CSS files, and intermediate build output, should be ignored. These files are typically generated from source code and don't need to be versioned.

2. **Dependencies:** Dependency directories or files generated by package managers (e.g., `node_modules/` for Node.js projects, `vendor/` for PHP projects) should be ignored. These directories contain third-party dependencies and can be large and contain numerous files that are unnecessary to version control.

3. **Temporary Files:** Temporary files, backup files, and editor-specific files (e.g., `.DS_Store`, `Thumbs.db`, `*.tmp`, `*.bak`, `*.swp`) should be ignored. These files are often generated by the operating system or text editors and are not essential to the project.

4. **Environment-specific Files:** Configuration files or environment-specific files (e.g., `.env`, `*.config`, `*.properties`) containing sensitive information or environment-specific settings should be ignored to prevent exposing sensitive data or environment configurations.

5. **IDE/Editor Configuration:** IDE or editor configuration files (e.g., `.idea/`, `.vscode/`, `.emacs.d/`) should be ignored. These files contain project-specific settings for development environments and may vary between developers.

Here's what not to add to a `.gitignore` file:

1. **Source Code:** Source code files (e.g., `.js`, `.css`, `.html`, `.php`) should not be added to `.gitignore` unless they are generated files. Source code is typically versioned and tracked in the repository to collaborate on and maintain the project.

2. **Important Configuration Files:** Configuration files that are crucial for the application to function (e.g., `package.json`, `composer.json`, `.gitignore` itself) should not be ignored. Ignoring these files can lead to inconsistencies and issues when collaborating on the project.

3. **License and Documentation:** License files (e.g., `LICENSE`, `COPYING`) and documentation files (e.g., `README.md`, `docs/`) should not be ignored. These files provide important information about the project's licensing, usage, and documentation and should be versioned to maintain project transparency and compliance.

By following these guidelines and maintaining a well-curated `.gitignore` file, developers can ensure that only relevant files are tracked and committed to the Git repository, leading to a cleaner version history and better collaboration among team members.

## Why should I not modify 'package-lock.json' ?

The `package-lock.json` file is automatically generated by npm (Node Package Manager) or Yarn when installing dependencies for a Node.js project. It serves as a lockfile, which means it provides a detailed and deterministic description of the exact dependency tree and version of every package installed in the project. Modifying the `package-lock.json` file directly is generally not recommended for several reasons:

1. **Dependency Consistency:** The purpose of the `package-lock.json` file is to ensure that all developers working on the project, as well as continuous integration (CI) or continuous deployment (CD) systems, use the same versions of dependencies. By modifying the lockfile manually, you risk introducing inconsistencies in dependency versions across different environments, which can lead to unpredictable behavior and bugs.

2. **Version Control:** The `package-lock.json` file is intended to be committed to version control along with other project files. By modifying it manually, you deviate from the deterministic state of dependencies that was established during installation. This can cause confusion and conflicts when collaborating with other developers or when deploying the project to different environments.

3. **Security and Stability:** The `package-lock.json` file plays a crucial role in ensuring the security and stability of the project. It locks down the exact versions of dependencies and their transitive dependencies, preventing unintended upgrades or downgrades that could introduce security vulnerabilities or compatibility issues. Modifying the lockfile can compromise the integrity of the dependency tree and expose the project to potential risks.

4. **Dependency Resolution:** npm and Yarn use the information in the `package-lock.json` file to perform dependency resolution during installation. By manually editing the lockfile, you bypass the dependency resolution mechanism and may inadvertently introduce inconsistencies or conflicts in the dependency tree.

While it's generally discouraged to modify the `package-lock.json` file manually, there may be exceptional cases where it's necessary, such as resolving specific dependency conflicts or addressing issues with package versions. In such cases, it's important to proceed with caution and carefully consider the implications of modifying the lockfile. It's usually preferable to address dependency-related issues through proper dependency management practices, such as updating package versions in the `package.json` file and allowing npm or Yarn to regenerate the lockfile automatically.

## What is 'node_module'? Is it a good idea to push that on git ?

The `node_modules` directory is a directory created by package managers like npm (Node Package Manager) or Yarn to store project dependencies. When you install dependencies for a Node.js project using npm or Yarn, the packages are downloaded and stored in the `node_modules` directory along with their dependencies.

Here are some key points about the `node_modules` directory:

1. **Dependency Storage:** The `node_modules` directory contains all the packages and their dependencies required by your Node.js project. Each package typically includes its own source code, as well as any additional files or assets it may require.

2. **Version Control:** It's generally not considered a good practice to include the `node_modules` directory in version control systems like Git. There are several reasons for this:
   - **Size:** The `node_modules` directory can be quite large, especially for projects with many dependencies. Including it in version control can significantly increase the size of the repository, leading to slower cloning and checkout times.
   - **Redundancy:** Since package managers like npm or Yarn already manage dependencies and can install them based on the `package.json` or `yarn.lock` files, there's no need to store the `node_modules` directory in version control. It's redundant and can be regenerated easily.
   - **Security:** Including the `node_modules` directory in version control can potentially expose sensitive information or introduce security risks if packages contain vulnerabilities. It's safer to rely on package managers to install dependencies from trusted sources.

3. **.gitignore:** Instead of including the `node_modules` directory in version control, it's common practice to add it to the `.gitignore` file. This tells Git to ignore the `node_modules` directory and its contents when tracking changes, preventing it from being committed to the repository.

4. **Package Restoration:** When setting up a project on a new machine or deploying it to a server, developers can use package managers like npm or Yarn to install dependencies based on the `package.json` or `yarn.lock` files. These tools will automatically recreate the `node_modules` directory and install the necessary packages.

In summary, while the `node_modules` directory is essential for managing project dependencies in Node.js projects, it's not recommended to include it in version control. Instead, rely on package managers to install dependencies based on configuration files, and use `.gitignore` to exclude the `node_modules` directory from being tracked by Git.

## What is the 'dist' folder ?

The `dist` folder is a conventionally used directory name in web development projects, short for "distribution." It is commonly used to store the final output or distribution of a project after it has been built or compiled. 

When you use Parcel, a popular JavaScript module bundler, to build your project, it typically generates the `dist` folder as the output directory by default. Inside the `dist` folder, you'll find the bundled and optimized files ready for deployment to a production environment. 

Here's what you might find inside the `dist` folder after running Parcel:

1. **Bundled JavaScript:** Parcel combines and bundles your JavaScript source files and their dependencies into one or more optimized JavaScript files. These files may be minified and may include additional optimizations such as code splitting, tree shaking, and dead code elimination.

2. **Compiled CSS:** If your project includes CSS files or preprocessors like Sass or Less, Parcel compiles them into CSS and bundles them into one or more CSS files. These CSS files may also be minified and optimized for production.

3. **HTML files:** Parcel may generate HTML files that reference the bundled JavaScript and CSS files. These HTML files are typically ready to be served to users and may include links to assets like images or fonts.

4. **Other assets:** Depending on your project configuration, the `dist` folder may also contain other assets such as images, fonts, or static files that are part of your project. Parcel may optimize these assets as well, for example by compressing images or optimizing SVG files.

Overall, the `dist` folder serves as the output directory for your project's production-ready files. Once your project has been built with Parcel, you can deploy the contents of the `dist` folder to a web server or hosting service to make your application available to users.

## What is 'browserlist' ?

The correct term you're referring to is "Browserslist," not "browserlists." Browserslist is a popular configuration file used by various front-end tools, such as Autoprefixer, Babel, PostCSS, and eslint-plugin-compat, to specify which browser versions and environments your project supports.

Here's how Browserslist works:

1. **Configuration File:** Browserslist typically uses a configuration file named `.browserslistrc`, `browserslist`, or specified within the `browserslist` field in `package.json`.

2. **Query Syntax:** In this file, you define a list of target browsers and their versions using a query-like syntax. For example, you might specify which versions of major browsers (e.g., Chrome, Firefox, Safari, Edge) your project should support.

3. **Support Definitions:** Browserslist supports various syntaxes for defining browser support, including usage data (based on global usage statistics), custom selection (specifying browser versions explicitly), and queries (using logical operators to define browser support).

4. **Tool Integration:** Front-end tools like Autoprefixer, Babel, and PostCSS use the Browserslist configuration to determine which vendor prefixes to add to CSS properties, which JavaScript syntax features to transpile, or which polyfills to include based on the targeted browsers.

Here's an example of a simple Browserslist configuration:

```
# Browsers that we support
last 2 versions
```

In this example, `last 2 versions` instructs tools to target the last two versions of each browser for compatibility.

By using Browserslist, developers can ensure that their web projects are compatible with a specified set of browsers and environments. This helps maintain consistency in rendering and behavior across different browsers while avoiding unnecessary polyfills or vendor prefixes for unsupported browsers.

## read about different bundlers: vite, webpack and parcel

Vite, Parcel, and Webpack are all popular build tools used in modern web development, but they differ in their approaches, features, and performance optimizations. Here are some of the major differences between Vite, Parcel, and Webpack:

1. **Development Server:**
   - Vite: Vite is known for its extremely fast development server, which leverages ES module (ESM) imports to achieve near-instantaneous hot module replacement (HMR) and fast build times. It uses native browser ES module support during development, resulting in rapid iteration and improved developer experience.
   - Parcel: Parcel also provides a built-in development server with support for hot module replacement (HMR) and fast rebuild times. It aims to simplify the development workflow with zero-configuration setup, making it easy to get started without complex configuration files.
   - Webpack: Webpack offers a development server with support for hot module replacement (HMR), but its performance may not be as fast as Vite or Parcel out of the box. Webpack's configuration-driven approach provides more flexibility but may require additional setup for optimal performance.

2. **Bundle Strategy:**
   - Vite: Vite utilizes an ES module (ESM) first approach, serving JavaScript modules directly to the browser during development. For production builds, Vite generates highly optimized ES modules and leverages native browser support for ES module loading.
   - Parcel: Parcel follows a zero-configuration strategy, automatically analyzing project dependencies and generating optimized bundles tailored for different environments (development vs. production). Parcel supports multiple output formats, including ES modules, CommonJS, and UMD.
   - Webpack: Webpack is a highly configurable module bundler that supports various module formats (e.g., CommonJS, AMD, ES modules) and offers extensive customization options through its configuration file (webpack.config.js). Webpack optimizes bundles for production by applying techniques such as code splitting, tree shaking, and minification.

3. **Configuration and Customization:**
   - Vite: Vite emphasizes simplicity and minimal configuration, providing a predefined configuration that covers common use cases out of the box. Advanced configuration options are available for customization, but the default setup is designed to be intuitive and easy to use.
   - Parcel: Parcel is known for its zero-configuration setup, which automatically handles various build tasks without requiring explicit configuration files. While Parcel supports customization through plugins and command-line options, it may not offer the same level of flexibility as Webpack.
   - Webpack: Webpack offers extensive configuration options through its webpack.config.js file, allowing developers to fine-tune the build process to their specific requirements. Webpack's plugin system and loaders provide additional customization capabilities, making it highly adaptable to different project needs.

4. **Performance:**
   - Vite: Vite is renowned for its exceptional performance, particularly during development, thanks to its use of native ES module loading and fast HMR. Vite's development server and build times are among the fastest in the industry, making it ideal for large-scale projects.
   - Parcel: Parcel also offers fast build times and supports hot module replacement (HMR) during development. While Parcel's performance is generally good, it may not match the speed of Vite's development server or build times.
   - Webpack: Webpack's performance depends on the complexity of the project and the configuration settings. While Webpack provides powerful optimization features, such as code splitting and tree shaking, configuring it for optimal performance may require additional effort compared to Vite or Parcel.

In summary, Vite, Parcel, and Webpack are all capable build tools with unique strengths and trade-offs. Vite excels in speed and developer experience, Parcel prioritizes simplicity and zero-configuration, while Webpack offers extensive customization and optimization options. The choice between them depends on factors such as project requirements, performance considerations, and developer preferences.

## read about ^ and ~

In the `package.json` file of a Node.js project, you might encounter the `^` and `~` symbols used to specify version ranges for dependencies. These symbols are part of the Semantic Versioning (SemVer) system and allow developers to define flexible version constraints for dependencies.

Here's what each symbol means:

1. **Caret (^):**
   - The caret symbol `^` is used to specify a range of compatible versions with the following rules:
     - If the specified version is `^x.y.z`, npm will install the latest minor and patch versions for the same major version `x`. For example, `^1.2.3` would allow npm to install any version from `1.2.3` to `1.9.9`, but it won't allow version `2.0.0` or higher.
     - It's essentially a "safety net" that allows for automatic updates to the latest minor and patch versions within the same major version without breaking changes. This is useful for ensuring that your project stays up-to-date with bug fixes and minor enhancements while avoiding major version upgrades, which may introduce breaking changes.

2. **Tilde (~):**
   - The tilde symbol `~` is used to specify a range of compatible versions with the following rules:
     - If the specified version is `~x.y.z`, npm will install the latest patch version for the same minor version `x.y`. For example, `~1.2.3` would allow npm to install any version from `1.2.3` to `1.2.9`, but it won't allow version `1.3.0` or higher.
     - It's similar to the caret symbol (`^`) but more restrictive, as it only allows for automatic updates to the latest patch versions within the same minor version. This is useful for ensuring that your project receives bug fixes and minor updates while maintaining compatibility with the same minor version.

Using these version range specifiers allows developers to balance the need for stability and compatibility with the desire to stay up-to-date with bug fixes and minor enhancements in dependencies. However, it's important to carefully consider the implications of using these symbols, as they may introduce unexpected changes or compatibility issues, particularly in larger or long-lived projects. It's often a good practice to specify exact versions (`1.2.3`) for critical dependencies or dependencies with known compatibility issues, while using version ranges for less critical or more flexible dependencies.

## Read about script types in html ?

In HTML, the `<script>` element is used to embed or reference JavaScript code within an HTML document. There are different ways to include JavaScript code using the `<script>` element, and they can be classified into several types:

1. **Inline Scripts:**
   - Inline scripts are JavaScript code that is directly embedded within the HTML document. This is done by placing the JavaScript code between `<script>` and `</script>` tags within the HTML file.
   - Example:
     ```html
     <script>
       alert("This is an inline script!");
     </script>
     ```

2. **External Scripts:**
   - External scripts are JavaScript code that is stored in separate files (with a `.js` extension) and then referenced in the HTML document using the `src` attribute of the `<script>` element.
   - Example:
     ```html
     <script src="myscript.js"></script>
     ```

3. **Deferred Scripts:**
   - Deferred scripts are external scripts that are loaded asynchronously while the HTML document is being parsed. They are executed after the document has been fully parsed and before the `DOMContentLoaded` event is fired.
   - Deferred scripts are indicated by adding the `defer` attribute to the `<script>` element.
   - Example:
     ```html
     <script src="myscript.js" defer></script>
     ```

4. **Async Scripts:**
   - Async scripts are external scripts that are loaded asynchronously while the HTML document is being parsed. They do not block the HTML parsing process and are executed as soon as they are downloaded, regardless of the order in which they appear in the document.
   - Async scripts are indicated by adding the `async` attribute to the `<script>` element.
   - Example:
     ```html
     <script src="myscript.js" async></script>
     ```

5. **Module Scripts:**
   - Module scripts are JavaScript modules that allow for modular code organization and encapsulation. They are indicated by adding the `type="module"` attribute to the `<script>` element.
   - Module scripts support the use of ES6 module syntax (`import` and `export` statements) and are loaded asynchronously.
   - Example:
     ```html
     <script type="module" src="module.js"></script>
     ```

Each type of script inclusion has its own use cases and implications for performance, loading behavior, and script execution order. Understanding these differences can help developers choose the appropriate method for including JavaScript code in their HTML documents based on their specific requirements and constraints.

# Episode 03: Laying the Foundation

## Creating Scripts for Start and Build

- Executing `npx parcel index.html` runs index.html using Parcel and creates a development build.
- We can create a script for this so that we don't need to write it repeatedly. It's an industry standard.
- To do this, go to [package.json](./episode-03-laying-the-foundation/package.json) and in the scripts section, add `"start": "parcel index.html"` and `"build": "parcel build index.html"`.
- Now, in the command line, we can simply execute `npm start` and `npm build` to run `npm parcel index.html` and `npm parcel build index.html`.
- **Tip:** If you're unsure how to start any large app, check the package.json scripts; they often provide guidance.
- `npm run start` == `npm start` but not for other commands.
- ```json
    "scripts":{
        "start":"parcel index.html",
        "build":"parcel build index.html",
        "test": "jest"
    }
    ```

## Episode 02 Revision

- Like in a browser where we can see the DOM element, similarly in React, we have React elements.
- We can create React elements using `React.createElement` as shown in [App.js](./episode-03-laying-the-foundation/App.js).
- **React.createElement** returns an object, not an HTML element.
- Syntax: `const var = React.createElement("element",{attributes}, "Content");`
- Eg: `const heading = React.createElement("h1",{id:"heading"}, "Namaste React");`
- So, in the above example, `heading` will be an object, also known as a React element.
- When we render this object to the DOM, it becomes an HTML element.
- Whatever happens inside React will happen inside the root, hence we need to create a root using react-dom.
- `const root = ReactDOM.createRoot(document.getElementById("root"));`
- Now, we will render the `h1` object in the root using `root.render(heading);`
- Hence **React.createElement => Object => HTMLElement(render)**

## JSX

- Writing code in JS is hard and not developer-friendly, so we use JSX.
- **JSX** is a JavaScript syntax that makes writing JS easier.
- **JSX** is not a part of React; we can write React without using JSX also.
- **JSX** tries to mix up HTML and JS to use it together.
- **JSX** is not HTML inside JS; it's HTML-like or XML-like syntax.
- A React element (object) using JSX: `const jsxHeading = <h1 id="heading">This is a JSX Heading</h1>;` 
- **Note:** jsxHeading === heading in [App.js](./episode-03-laying-the-foundation/App.js)

## JSX Working

- JS Engine understands ECMAScript; it does not understand JSX.
- Parcel is transpiling the JSX to JS code and sending it to the JS engine. It's not doing this itself.
- Parcel is a bundler; it assigns this job to the Babel Compiler.
- **Babel** is doing it. It's a JS compiler. It converts JSX => React.createElement.
- **JSX** -> **Babel** => **JS** => **React.CreateElement** => **Object** => **render** => **HTML**
- Visit [Babel.js](https://babeljs.io/) to see how Babel works.

## JSX Syntax

- We write JSX attributes in camel case. Eg: `className`
- If we write JSX in multiple lines, we need to wrap it inside `()`.
- JSX code can have only 1 parent element. Otherwise, we need to wrap it inside `<div></div>` or `<></>`

## React Components

- In React, everything is a component.
- In React, we have 
    - **Class-based component**: The old way of writing code. It uses JS classes.
    - **Functional component**: It uses JS functions.
- **React Functional Component** is a basic JS function that returns some JSX code or a group of React elements.
- **Component composition**: Writing a component inside another component.
- **Always write Component Name in capital letters.** 
- We can also use normal functions, but we need to ensure that it returns the JSX.
- For rendering components, we need to write the component name inside `<></>`. Eg: `root.render(<Heading/>)`
- When creating a component, we can either directly return the JSX, in which case we use `()`, or we need to use `{}` and inside it return the JSX.
- Check **HeadingComponent1** and **HeadingComponent3** in [App.js](./episode-03-laying-the-foundation/App.js) for better understanding.
- We can write any JS code using `{}` inside JSX; hence, before we return JSX in a component, we are able to write JS code in a component.
- We can also write JS inside JSX using `{}`

## JSX Benefits

- Suppose we have `const data = api.getData()` and the attacker is sending some malicious data into it. If we're using this `data` variable inside our React component, this attack is known as **cross-site scripting**. JSX takes care of these injection attacks.
- JSX sanitizes malicious data.
- We can write a component in the following ways: `<Title/>` ==== `<Title><Title/>` === `{Title()}`

# Episode 04: Talk is cheap, show me the code!

## Food ordering App

- The first this always is to plan. Then only start writing the code.
- Try to build the wireframe. Think about the components
- The following will be our general layout:
    - header
        - logo
        - nav Items
        - about
    - Body
        - Search
        - restaurant container
        - restaurant card
            - image
            - rating
            - price
            - delivery time
    - footer
        - Copyright
        - Links
        - Address
        - Contact

## CSS

- the inline styles will be an object.
- Eg: `style={{backgroundColor: "grey"}}`
- The outer bracket denotes that its JS code, the inner bracket denotes that its a n object.
- This is same as writing:
- ```
    const s ={
    backgroundColor: "grey"
    };

    style={s}
    ```

## Props

- props is a short form for properties.
- they are arguments to the functional components.
- We use it to passing dynamic data.
- we can pass any number of props.
- writing the prop names at the `()` is called **destructuring on the fly**.
- eg: `const abc = ({prop1, prop2}) => {...};`
- We can also write it like `const {prop1, prop2} = props;`

## How does data comes in Big Apps ?

- Go to [swiggy.com](swiggy.com) and click on inspect -> network tab -> Fetch/XHR.
- You will see the v5?lat API , in that go to the preview -> data section.
- **Config driven UI**: swiggy data
- UI + data = frontend.

##  Key and Map

- key is a unique keyword and we should always use it whenever we are using map.
- It takes a big peformence hit if we dont add a key because **it renders all object elements**.
- We can also use index as the key. 
- This index is the property of the map. 
- It logically looks right, but react itself says that **we should not use index as keys in react**
- **Index  as a key is an anti pattern**
- If we dont have a unique ID, we can use indexes but it is not recommended.







