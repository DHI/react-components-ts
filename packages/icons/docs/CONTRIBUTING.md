First of all, welcome and thank you for contributing to our Storybook.

# About

The purpose of our `@dhi/icons` GitHub library is to host the icons developed by the UI/UX department which are used extensively within DHI.

An icon component with low usage either means that it isn't fully working yet or that there is a low demand for it.

# Setting up

To get started follow these steps:

- Clone the repository.
- Change your working directory to `packages/icons`
- Install dependencies `yarn install`.


## Adding an icon

When adding an icon, make sure that:
* [x] Add `.svg` icon files in the `src` folder.
* [x] The file names should be written in `kebab-case` and the SVG is recommended to be `40px x 40px` in size.

## Commits:

We are using the [Angular Commit Message Conventions](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines) for versioning our packages.

| Commit messages            | Release type           |
| -------------------------- | ---------------------- |
| fix(name): Commit message  | Patch Release 0.0.1    |
| feat(name): Commit message | Feature Release 0.1.0  |
| perf(name): Commit message | Breaking Release 1.0.0 |

Each of these commits will trigger a specific semantic versioning action when in the pipeline, so use with precaution.

## Branch naming conventions

- `fix/branch-name` - When dealing with a bug or a quick-fix
- `feature/branch-name` - When dealing with a feature
- `docs/branch-name` - When dealing with the documentation

## Issues

When creating a new feature, its necessity and value should initially be evaluated.
This is done by creating an issue and describing how does the feature improve our current icons package and what is the expected behaviour, assign somebody to it and label it accordingly.

In order for a component to be added, it needs to check a few boxes:

* [x] The component implements an element of the [DHI Design Guidelines](https://www.figma.com/file/pSfX5GNsa6xhKGbi3DWQtn/DHI-Official-Guidelines) or is otherwise generic enough in functionality and close enough to the DHI CVI that it is likely to find reuse in other projects.
* [x] The component needs to be reviewed by at least one of the maintainers.


## Pull Requests (PR)

When creating a PR, please explain the need of the icon and make sure to link the relevant GitHub issues.

Moreover, ensure that you are going through the PR template instructions.

## Dependencies, devDependecies and peerDependencies

- dependencies

Inside the `dependencies` we want to include all the production external libraries we are using. The whole concept around it is that when a developer installs our package, `npm` needs to know what other dependecies to install inside `node_modules`, without requiring the developer to install it inside it's own app dependencies.

- peerDependencies

The `peerDependencies` are the dependencies that the developers using our package need to install alongside our package.

- devDependencies

While developing, we are primarily using the `devDependencies` to develop the library. Any dependencies that are needed for the development should be added here.

## Building / Exporting

Icons are generated with the `build-icons.js` Node.js script, found in the root of the icons package.  
It first generates TypeScript JSX React icon components from a template, then compiles them with TypeScript into `.js` and `.d.ts` files

## Testing

- to be added

Thank you for contributing!
