# CI/CD

As for the choice of the tool to use for continuous integration and continuous development, the choice is difficult and influenced by several factors. The tools that I have identified as eligible are the following:

- [Ansible](https://www.ansible.com/) - is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT tasks such as continuous deployments or zero downtime rolling updates
- [Circle CI](https://circleci.com/) (allows you to do Continuous Integration and seems to be very simple to use and similar to Github Actions)
- [Travis CI](https://travis-ci.org/) (allows you to do Continuous Integration and seems to be very simple to use and similar to Github Actions)
- [GitLab CI / CD](https://docs.gitlab.com/ee/ci/) (used to make CI / CD on GitLab, as the two tools above, namely Circle CI and Travis CI, do not have integration with GitLab at the moment, but only with GitHub and Bitbucket)
- [Github Actions](https://docs.github.com/en/actions/get-started/)

## Travis CI
Travis CI is a tool that deals with Continuous Integration & Deployment. It is very simple to use and configure and supports many programming languages ​​and platforms: Android, C, C #, C ++, Clojure, Crystal, Dart, Erlang, Elixir, Go, Groovy, Haskell, Haxe, Java, JavaScript (Node.js ), PHP, Python, Ruby, Scala and Visual Basic. Offers integration with Bitbucket and GitHub platforms (not with GitLab). The plans it offers are as follows:

- Free
    - 100 builds allowed in total (not per month)
    - Supports OS: Windows, Linux, MacOS, FreeBSD
    - No concurrent jobs
- Bootstrap
    - Supports OS: Windows, Linux, MacOS, FreeBSD
    - One concurrent job
    - Unlimited builds
- Advanced
    - Supports OS: Windows, Linux, MacOS, FreeBSD
    - Two simultaneous jobs
    - Unlimited builds
- Premium
    - Supports OS: Windows, Linux, MacOS, FreeBSD
    - Five simultaneous jobs
    - Unlimited builds

Travis CI also has the following features:

- Use Yaml for configuration files
- It is cloud-based
- Use Docker to run tests
- It is great for small and medium-sized projects

## Circle CI
The strength of Circle CI is that it has many integrations with platforms such as: GitHub, Bitbucket, Slack, AWS, Azure, Serverless, Jira etc. and is used by large companies such as Facebook, Kickstarter, Spotify and GoPro. However, it supports fewer languages ​​than Travis CI, specifically it can be used with: C ++, Javascript, .NET, PHP, Python, Ruby, Java, Go. Other strengths of Circle CI are:

- It is easy to use and configure
- Use Yaml for configuration
- It is cloud-based, but also gives the possibility to install it on local machines
- Great documentation

Floor-level, Circle CI looks really great:

- Free
    - 2,500 credits / week that are used as "money" for the use of the server and builds
    - One concurrent job
    - Build on Linux / Windows
- Performance ($ 30 + / month)
    - 25,000 credits / week
    - $ 15 / month for the first three users
    - Build on Linux / macOS / Windows
- Scaling (is the custom floor)

## GitLab CI / CD
GitLab also allows you to do Continuous Integration / Delivery / Deployment. Its operation is similar to GitHub Actions, pipeline configuration is done through a yaml configuration file. Since our repositories are mainly present on GitLab, it could be a valid solution to adopt, so as to concentrate project management and deployments in a single platform.
GitLab also has paid plans which are as follows:

- Free
    - 400 minutes CI / CD
- Starter ($ 4 / user / month)
    - all the features of the Free version
    - Single-team project management
    - 2000 CI / CD minutes
    - Technical support
- Premium ($ 19 / user / month)
    - all the features of the Starter version
    - Cross-team project management
    - 10000 CI / CD minutes
    - Priority in technical support
- Ultimate ($ 99 / user / month)
    - all the features of the Premium version
    - 50000 CI / CD minutes
    - Free guest users
    - Advanced application security