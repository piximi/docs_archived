---
description: An overview of Scripts and Lerna
---

# Scripts & Lerna

### Scripts

#### bootstrap

Use the `bootstrap` command to bootstrap the packages found in the ./packages directory:

```text
yarn bootstrap
```

#### build

Use the \`build\` command to build the packages found in the ./packages directory:

```text
yarn build
```

#### clean

Use the `clean` command to clean the build artifacts created by “build.”

```text
yarn clean
```

#### test

Use the \`test\` command to run the unit tests found in the packages in the ./packages directory:

```text
yarn test
```

### Dependencies

Use the `lerna add` command to add a dependency to one or more packages.

If a dependency is used by just one package, use the `scope` option to specify the correct package name. For example:

```text
lerna add foo --scope=@piximi/bar
```

adds the \`foo\` package to the decencies of the \`@piximi/bar\` package.

If a dependency is used by more than one package, use the \`scope\` option to specify the correct packages and provide the \`peer\` option to specify that the package is a peer dependency. For example:

```text
lerna add foo --peer --scope=@piximi/bar, @piximi/baz
```

adds the `foo` package to the peer dependencies of both the `@piximi/bar` and `@piximi/baz` package.

