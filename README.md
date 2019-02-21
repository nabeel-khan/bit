
<p align="center">
  <a href="https://bitsrc.io"><img src="https://storage.googleapis.com/bit-docs/component-discovery-bit-react-gif.gif"></a>
</p>


  <a href="https://opensource.org/licenses/Apache-2.0"><img alt="apache" src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"></a>
  <a href="https://github.com/teambit/bit/blob/master/CONTRIBUTING.md"><img alt="prs" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
  [![Gitter chat](https://badgen.now.sh/badge/chat/on%20gitter/cyan)](https://gitter.im/bit-src/Bit)
  [![Discourse status](https://img.shields.io/discourse/https/meta.discourse.org/status.svg)](https://discourse.bitsrc.io/)
  <a href="https://github.com/teambit/bit/blob/master/CHANGELOG.md"><img alt="Appveyor Status" src="https://ci.appveyor.com/api/projects/status/vg7wvfvku12kkxkc?svg=true"></a>
  <a href="https://github.com/teambit/bit/blob/master/CHANGELOG.md"><img alt="Circle Status" src="https://circleci.com/gh/teambit/bit/tree/master.svg?style=shield&circle-token=d9fc5b19b90fb7e0655d941a5d7f21b61174c4e7">
[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Share%20code%20components%20as%20a%20team%20@bit_src&url=https://bitsrc.io&hashtags=opensource,javascript,programming,reactjs,webdev,vuejs,angularjs)

[Website](https://bitsrc.io) • [Docs](https://docs.bitsrc.io) • [Video](https://www.youtube.com/watch?v=P4Mk_hqR8dU) • [Blog](https://blog.bitsrc.io/) • [Gitter](https://gitter.im/bit-src/Bit) • [Discourse](https://discourse.bitsrc.io/) • [Examples](https://bitsrc.io/bit/movie-app)

## About  

**Bit helps you share, discover and compose components to build faster**.  

Bit integrates to **Git** and package managers **(npm/yarn)** to bring a better experience for sharing code between apps and developers.  

it eliminates the overhead around code sharing  by letting you quickly share and reuse components without boilerplating, refactoring or configurations. It then helps you track and sync changes across your codebase.  

It provides discoverability and collaboration over components through [Bit’s community hub](https://bitsrc.io/components).  

*Bit is a collaborative open source project, actively developed and maintained by a venture-backed team and used by more teams and communities every day*.  

## Contents  

- [Examples](#examples)
- [Getting started](https://bitsrc.io)
- [Docs](https://docs.bitsrc.io)
- [Workflow](##workflow)
  - [Bit monorepo](#bit-monorepo)
  - [Bit between apps](#bit-between-repos)
  - [Bit component design system](bit-component-design-system)
- [Motivation](#motivation)
- [Contributing](#contributing)  

## Examples  

Bit can be used to share and reuse code from any JavaScript project. Every component can be installed, used and even developed in any other project. Popular use cases are [UI components](https://bitsrc.io/components?labels=ui%20components), [React components](https://bitsrc.io/components?labels=react), [NodeJS and utility functions](https://bitsrc.io/components?labels=utils) and more.  

### UI components

Share components from UI libraries and projects, and use them to build new apps.  

**React spinners**:  

<p align="center">
  <a href="https://bitsrc.io/bondz/react-epic-spinners"><img src="https://storage.googleapis.com/bit-docs/react-spinners-bit-ui-gif.gif"></a>
</p>  

[GitHub Repository](https://github.com/bondz/react-epic-spinners) → [Components with Bit](https://bitsrc.io/bondz/react-epic-spinners).  

Once you choose a component, you can play with it in a live playground, save examples, and use npm/yarn to install it in your project.  

<p align="center">
  <a href="https://bitsrc.io/davidhu2000/react-spinners/pacman-loader"><img src="https://storage.googleapis.com/bit-docs/react-pacman-loader-ui-gif.gif"></a>
</p>  

### Plain JavaScript and NodeJS

Share components from JavaScript libraries and projects, and use them to build new apps.   

**Ramda functions**:  

<p align="center">
  <a href="https://bitsrc.io/ramda/ramda"><img src="https://storage.googleapis.com/bit-docs/ramda-functions-bit-gif2.gif"></a>
</p>  

[GitHub repository]() → [Functions with Bit](https://bitsrc.io/ramda/ramda).

## Workflow

Bit turns components into isolated and reusable building blocks you can run and develop from any other project in any context. It works in any given repository structure, without changing it at all, so the repository’s structure will remain the same.  

### Component isolation   

When running the `bit add` command Bit will isolate components in the existing project structure. Meaning, Bit will [track the components](https://docs.bitsrc.io/docs/add-and-isolate-components.html) and create a dependency graph for each of them. With this data, Bit creates an isolated environment for each component, which lets the component run and work in any other project.  

Then, you can `tag` the [components’ version](https://docs.bitsrc.io/docs/tag-component-version.html) and `export` them to a [remote collection](https://docs.bitsrc.io/docs/organizing-components.html) from which they can be installed in other projects.  

**Exporting 256 Radma components (functions) from the repository to Bit’s hub in 2 minutes**:  

<p align="center">
  <a href="https://www.youtube.com/watch?v=pz0y2GTsSrU"><img width="460" height="300" src="https://storage.googleapis.com/bit-docs/image-ramda-256-components.png"></a>
</p>  

### Component reuse  

Once components are shared to Bit’s hub (which isn’t mandatory; Bit is distributed and you can [set up a collection](https://docs.bitsrc.io/docs/bit-on-the-server.html) on any server), you can use them in other projects in a number of methods:  

[Install components with NPM and Yarn](https://docs.bitsrc.io/docs/installing-components.html)
[Import components with Bit](https://docs.bitsrc.io/docs/sourcing-components.html)  

#### Installing components with npm/yarn

You can install components shared to [Bit’s hub](https://bitsrc.io/components) from Bit’s package registry via the NPM or Yarn clients.  

#### Importing components with Bit

You can import components shared to [Bit’s hub](https://bitsrc.io/components) using the `bit import` command. This will [source the component](https://docs.bitsrc.io/docs/sourcing-components.html) in your local project, so you can [continue to develop it](https://docs.bitsrc.io/docs/modifying-sourced-components.html) right from the consuming project. Since Bit will keep tracking the component, you can [update](https://docs.bitsrc.io/docs/update-dependencies.html) and [sync](https://docs.bitsrc.io/docs/merge-changes.html) changes from your project to Bit’s hub (and if you wish, eject the component to become a package dependency) and to other projects.  

### Distributed component development

Relying on Bit’s ability to [import component](#importing-components-with-bit) into any project, you can develop the same component from different projects at the same time.  

This creates a distributed workflow in which your team can collaborate and suggest new updates for each other’s components, so that they can be extended over time. It also lets you control permissions for who can update which component, rather than being limited by access to the library from which the components were shared from.  

### Bit monorepo

Any repository or library containing components is already a Bit monorepo.  

Adding Bit to the repository will not change its structure, source code or configurations. You won’t need to refactor or create separate directories and configurations for every components.  
Instead, you can use Bit to track and share the components from your library directly to Bit’s hub. Then, they become availabe to install as NPM packages. This means that your React UI library + Bit will become a monorepo from which components can be individually discovered and installed, without changing the library. Component dependencies will be automatically defined by Bit, and build/test configurations will be [applied to all the components](https://docs.bitsrc.io/docs/building-components.html) using [Bit’s environments](https://bitsrc.io/bit/envs).  

#### Example:

Semantic UI library before Bit

Semantic UI React library with Bit

Semantic UI React components: Choose, play, use.


#### [Bit with and without Lerna](https://blog.bitsrc.io/monorepo-architecture-simplified-with-bit-and-npm-b1354be62870)

### Bit component design system

Bit is a quick and effective way to create a design system from your components.  

You can organize components for your team to share, try hands-on in Bit’s hub component playground (useful for designers), and use in your projects.  

Developers, designers and other team members can find, view and work with shared components to build faster together. [Learn more](https://blog.bitsrc.io/building-a-consistent-ui-design-system-4481fb37470f).

### Bit across repositories

Bit helps your team share and develop components between different projects to build multiple applications and products.

You can share components from repository A, then install or import them into repository B, make changes from repository B, and sync them back to repository A and to new repositories.

## Contributing

Contributions are always welcome, no matter how large or small. Before contributing, please read the [code of conduct](CODE_OF_CONDUCT.md).

See [Contributing](CONTRIBUTING.md).

## Feedback

Feedbacks and questions are more than welcome via Bit's [Gitter channel](https://gitter.im/bit-src/Bit) or [Discourse boards](https://discourse.bitsrc.io/).

## License

Apache License, Version 2.0

![Analytics](https://ga-beacon.appspot.com/UA-96032224-1/bit/readme)
