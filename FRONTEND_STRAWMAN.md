# Front end tech guidelines for the the Identity team

This document captures frontend technical preferences for the Identity IDP
project. The list of recommendations may be of interest to other projects too.

## About this document

This document is a set of current, effective frontend project technology
recommendations that were determined via discussions with number of front end
developers within the DTO. Following these guidelines should not be an
_obligation_.  Use what works best for the team and the project.

Thanks to Nathan Flew, Elise Chant, Jonothan Conway and Phillip Piper for
providing great feedback and suggestions.

## Recommendations

### Use React

### Use `create-react-app` to create new React applications

Stop yak shaving & bike shedding. Use the official way to create an app. The
defaults are decent.

### Can use any JS features supported by `create-react-app` defaults

### Optionally use Flow for static typing

It is included with `create-react-app` and just needs a few lines of config to
enable it. Using it should not be mandatory. (Other compile-to-JS languages
should not be used).

### Testing: use Jest

### Testing: use Enzyme for testing React components

### Write stateless React components

### Build the component gallery with `react-storybook`

Build gallery pages for your components that show the various different states
and options.

### Prefer Redux for state management

An immutable global state makes a React application easier to reason about. The
Redux Dev Tools chrome plugin is *excellent*.

### Consider using `redux-forms` for managing forms

### Consider using an immutable data structure library

`seamless-immutable.js` has stronger guarantees. `immutable.js` has a richer API.

### Use react-router

### Use `npm shrinkwrap`

Especially if you run node in production (rather than simply being part of your
development toolchain).

`npm install` without a shrinkwrap is non-deterministic because the dependency
graph can be resolved within the wiggle room that semantic versioning allows.
This is true even if the versions in your `package.json` are locked down,
because the transitive dependencies won't be.

Use shrinkwrap to capture your dependencies (including transitive dependencies).

Practically speaking, this means the same bytes will be installed in your
development environment as in CI as in staging as in production as well as in
your development environment (less "it works on my machine!", more robustness).

### Code organisation

Instead of organising code into top level folders for components, styles,
containers etc, organise your repository by _feature_.  These articles are
worth reading:

[How to better organize your React applications](https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1#.efx9fhmli)

[Organizing large React applications](http://engineering.kapost.com/2016/01/organizing-large-react-applications/)

[Organizing Redux applications](http://jaysoo.ca/2016/02/28/organizing-redux-application/)

[React directory struture](http://marmelab.com/blog/2015/12/17/react-directory-structure.html)

### Consider using CSS Modules for component styling

https://github.com/css-modules/css-modules

