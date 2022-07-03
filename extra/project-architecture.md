# Project Architecture

Here are some tools and guidelines regardless of the type of language or project you are working with.

## Code quality and static analysis

In each project insert the .editorconfig file where you need to specify the configuration to be used within the editor. The configuration I thought of is the following:

```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 4
trim_trailing_whitespace = true
insert_final_newline = true
end_of_line = lf
max_line_length = off

[**.php]
indent_size = 4

[**.md]
indent_size = false
```

## Utility

- [Husky](https://github.com/typicode/husky) - library to automate scripts during commits and more
- [Storybook](https://storybook.js.org/) - open source tool for developing UI components in isolation
- [Bit.dev](https://bit.dev/) - scalable and collaborative way to build and reuse components
- [Hotjar](https://www.hotjar.com/) - web analytics tool that help you analyze traffic data monitoring users actions
- [LogRocket](https://logrocket.com/) - tool to track errors, user experience and performance metrics on the FE (only JavaScript)
- [Sentry](https://docs.sentry.io/) - tool to track errors and issues for many language codes (BE and FE). It has integration with ClickUp, Jira, Gitlab, Github ecc. to create issues
- [Responsively](https://responsively.app/) - allows you to view and test a web app on multiple devices simultaneously, also testing its features in terms of accessibility
- [gitignore.io](https://www.toptal.com/developers/gitignore) - generate useful .gitignore files for your project
- [github-changelog-generator](https://github.com/github-changelog-generator/github-changelog-generator) - tool to generate changelog automatically
- [readme-md-generator](https://github.com/kefranabg/readme-md-generator) - tool to generate readme automatically
- [Quokka](https://quokkajs.com/) - productivity tool for rapid JavaScript / TypeScript prototyping
- [Snyk Code](https://snyk.io/product/snyk-code/) - Give alerts of critical bugs in your IDE or upon every pull request