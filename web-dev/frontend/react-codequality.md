# React Code Quality

## Helpers

### StrictMode

- [More](https://reactjs.org/docs/strict-mode.html)

A tool that helps highlight any problems in the application. Just wrap the application or part of it between the tag

```
<React.StrictMode> {...} </ React.StrictMode>
```

to identify:
- Use of deprecated or insecure functions or methods
- Any unwanted effects

### Static type checking: Flow & Typescript

- [More](https://reactjs.org/docs/static-type-checking.html)

Uses type checking tools helps to resolve any errors before even running the application. If VSCode works together, they also improve the developer's life by offering features such as auto-completion.

### ESLint & Prettier

create-react-app and the frameworks based on React, bring with them a configuration of ESLint in the form of a package or a preconfigured file.
An example of custom configuration for NextJS + TypeScript is available at the following links: [.eslintrc](https://gist.github.com/Slexom/90d86f9961f5537c547a111c6f5a25e3), [package.json](https://gist.github.com/Slexom/24901346ddc73c065fb229a1978077eb). The configuration can easily be adapted for projects that do not require TypeScript or are not NextJS based.


ESLint config: [eslint-config-react-app](https://www.npmjs.com/package/eslint-config-react-app)

Prettier config:
*.prettierrc*

```
{
    "tabWidth": 4,
    "useTabs": true,
    "seeds": true,
    "singleQuote": true,
    "jsxBracketSameLine": false,
    "arrowParens": "avoid",
    "printWidth": 120
}
```

In order to avoid conflicts between the two tools and their rule sets, it is recommended to add the following package: [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier).

## Airbnb React / JSX Style Guide
Eslint guidelines and rules to always keep in mind for React and JSX:
https://airbnb.io/javascript/react/

## App Structure

The structure of a React-based project may differ based on the use of a framework and which one is used.

- React: https://reactjs.org/docs/faq-structure.html
- GatsbyJS: https://www.gatsbyjs.com/docs/reference/gatsby-project-structure/
- NextJS: https://medium.com/@pablo.delvalle.cr/an-opinionated-basic-next-js-files-and-directories-structure-88fefa2aa759


## Apply styles to a component

In React there are various ways to apply a set of style rules to a component: CSS / SASS / LESS, CSS modules and styled-components.

### Styled Components

- [Homepage](https://styled-components.com/)

The ease, reusability and dynamism of the custom components, the SSR support, the SASS syntax and many other aspects make styled-components a must have for every project.

## State management

Managing the states of an application is a very important and delicate part. The wrong approach can involve extra and unnecessary work.

### Redux

Among the various solutions that can be used with React, Redux, and the entire ecosystem of extensions, it is the most used and consolidated.
It is also advisable to use a middleware for the management of the side-effects such as redux-saga that makes use of generators.
The following image summarizes how a react application should manage status updates (I recommend reading this [Link](https://medium.com/vlk-studio/redux-fromscarso2king-3-la-folder-structure-6ae4eee631af) article).

### Recoil

- [Homepage](https://recoiljs.org/)

Depending on the needs of the application, however, the use of Redux can be excessive.
Recoil is a lightweight state manager who “thinks like React”. A state fragment, called **atom**, can be read and written by any component through the use of the useRecoilState hook, in a very similar way to useState. The component is implicitly subscribed to that atom so that each change of state renders the component updated.
A selector represents a state fragment to which a transformation has been applied. You can access the derived value through the useRecoilValue hook.

# Test

## Jest

[Homepage](https://jestjs.io/)

The test runner recommended by the React documentation. Compared to a browser, it offers a limited environment and an approximation of the DOM. The ability to test events occurs by simulating interactions. The tool offers the possibility to have mockups of modules or functions if necessary.


## React Testing Library

[Homepage](https://testing-library.com/docs/react-testing-library/intro)

A set of utilities, to run alongside Jest, written on react-dom and react-dom / test-utils that make the tests work on DOM nodes. This makes it easier to find elements within the component by querying the elements of the DOM itself or including texts, labels or, the recommended method, data-testid attributes. Events, such as "click" or "submit", can be triggered through the fireEvent helper.

## Mock Service Worker (MSW)

[Homepage](https://mswjs.io/)

Mock of REST or GraphQL requests.

## Coverage

IDEs allow you to see the coverage level directly on the tested file. Webstorm has the functionality already integrated, VSCode needs the Jest plugin and a minimum of configuration.


## Possible problems

One of the problems encountered is related to the use of styled-components. It may happen that a snapshot test fails due to the different class name generated by the library at the time of the test. The cause of the name diversity can vary. To overcome this problem, and to have a clearer view of the style changes, a package is available, [jest-styled-components](https://www.npmjs.com/package/jest-styled-components), which includes the style in the snapshot and replaces the class with a placeholder.