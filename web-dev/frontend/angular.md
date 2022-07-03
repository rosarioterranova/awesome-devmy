# Angular

## Articles
- [Best practices for a clean and performant Angular application](https://www.freecodecamp.org/news/best-practices-for-a-clean-and-performant-angular-application-288e7b39eb6f) - A list of best practices to write clean and performant Angular applications
- [Angular onPush Change Detection Strategy](https://netbasal.com/a-comprehensive-guide-to-angular-onpush-change-detection-strategy-5bac493074a4) - A Comprehensive Guide to Angular onPush Change Detection Strategy
- [NgRx + Facades](https://thomasburlesonia.medium.com/ngrx-facades-better-state-management-82a04b9a1e39) - NgRx + Facades: Better State Management
- [Angular scalable folder structure](https://itnext.io/choosing-a-highly-scalable-folder-structure-in-angular-d987de65ec7) - How to define a highly scalable folder structure for your Angular project
- [Push-based Architectures with RxJS](https://thomasburlesonia.medium.com/push-based-architectures-with-rxjs-81b327d7c32d) - How to implement Push-based Architectures with RxJS
- [View Facades + RxJS](https://medium.com/angular-in-depth/angular-you-may-not-need-ngrx-e80546cc56ee) - The power of View Facades with RxJS
- [How to get the most from the TypeScript compiler](https://levelup.gitconnected.com/how-to-get-the-most-from-the-typescript-compiler-angular-aae7fb53e0cf) - Use TypeScript compiler like a PRO
- [Get equipped with the right Typescript tooling in Angular](https://levelup.gitconnected.com/get-equipped-with-the-right-typescript-tooling-angular-6f789e222b30) - Improve your development experience by enriching your Angular's toolbox

# Codestyle

To get the most out of Angular projects it is important to first perform a correct configuration.

## Code Quality & Static Analysis
During the creation of the project we can use the Angular **strict mode**, which automatically sets TypeScript in strict mode. To do this, follow this simple [guide](https://indepth.dev/posts/1402/bulletproof-angular). Angular's strict mode does not enable some important configurations that we can manually set in the **tsconfig.base.json** file

To configure Angular to use ESLint and Prettier you can see a configuration example at the following [link](https://dev.to/gsarciotto/migrating-and-configuring-eslint-with-angular-11-3fg1)

## Folder Structure
In any software project it is important to give a certain structure and Angular projects are no exception. A good structure of Angular projects can be the following:

* app
    * modules
        * auth
            * components
            * data-transfer-objects / models
            * guards
            * pages
            * services
            * store
                * actions
                * effects
                * reducers
                * selectors
                * index.php
            * auth-routing.module.ts
            * auth.module.ts
    * core (should contain singleton services, universal components and other features where there’s only once instance per application)
    * shared (is where any shared components, pipes / filters and services should go)
    * app-routing.module.ts
    * app.component.html
    * app.component.scss
    * app.component.ts
    * app.module.ts
* assets
    * i18n
    * style (general stylesheet)
* environments
    * environment.prod.ts
    * environment.ts

For more details on the structure of projects in Angular, refer to the following [link](https://javascript.plainenglish.io/how-to-structure-angular-apps-in-2021-a0bdd481ad0d)

## Best Practices

Here are some best practices to follow to improve the performance and readability of projects in Angular:

- [Best practices for a clean and performant Angular application](https://www.freecodecamp.org/news/best-practices-for-a-clean-and-performant-angular-application-288e7b39eb6f/)
- [NgRx + Facades: Better State Management](https://thomasburlesonia.medium.com/ngrx-facades-better-state-management-82a04b9a1e39)
- [View Facades + RxJS](https://medium.com/angular-in-depth/angular-you-may-not-need-ngrx-e80546cc56ee)
- Set OnPush as default change detection strategy:
`ng config schematics. @ schematics / angular.component.changeDetection OnPush`
- Add command for the hot module replacement inside the package.json: `"start: hmr": "ng serve --hmr"`
- To improve the build speed of the Angular application, add the following environment variable before running `ng serve` or `ng build`:
- `"serve": "NG_PERSISTENT_BUILD_CACHE = 1 ng serve"`
- `"build": "NG_PERSISTENT_BUILD_CACHE = 1 ng build"`

## UI framework

As for the UI of projects in Angular, I would recommend the use of two standard libraries, at least for the creation of user dashboards:

- [Angular Material](https://material.angular.io/) - material Design components for Angular
- [angular-flex-layout](https://github.com/angular/flex-layout) - provides HTML UI layout for Angular applications
- [ngx-datatable](https://github.com/swimlane/ngx-datatable) - a feature-rich yet lightweight data-table crafted for Angular

In the event that the Angular project requires a more complex and customized graphical interface, I would opt for the use of a utility-first library such as [Tailwind](https://tailwindcss.com/) which from v12 can be installed using the command: `ng add ngx-tailwind`

## Nx DevTools
I wanted to insert a separate section only for [Nx](https://nx.dev/) given the vastness of the instrument. From what I have learned, it is a very solid tool for the creation of single-piece in which perhaps there is the FE part in Angular / React and the BE part in Node (although it is not essential). It allows you to start an Angular application with the best tools to use (ESLint, Prettier, Jest, Cypress, Storybook etc.) and in addition it allows you to manage the code, through the creation of libraries, in an easier and faster way, even if this implies a structure of files and folders that is a little more complex and not easy to digest at first glance, but with the benefit of having a more “shareable” code. It also has features for viewing a dependency tree and caching compiled files, to speed up the build process. In summary, it is a very valid tool, but strongly aimed at large projects where there is a need to manage an entire system through a single repository.

## Utility

Below is a set of libraries that can be very useful within any Angular project:

- [Compodoc](https://github.com/compodoc/compodoc) - documentation tool to generate a static documentation
- [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=it) - chrome's extension to debug application's state changes
- [Angular DevTools](https://chrome.google.com/webstore/detail/angular-devtools/ienfalfjdbdpebioblfackkekamfmbnh) - a DevTools extension for debugging Angular applications
- [source-map-explorer](https://angular.io/guide/deployment#inspect-the-bundles) - tool for measuring Angular performance