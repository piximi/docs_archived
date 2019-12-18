---
description: Writing code for packages
---

# Packages

## Mission

The aim of Piximi’s multi-package organization is three-fold:

* maintain a DRY codebase; 
* ensure generic interfaces between features; and 
* simplify the bootstrapping process for new contributors.

#### DRY

If you find yourself duplicating code, it’s time to create a new package. Packages like `@piximi/components`, `@piximi/store`, and `@piximi/types` exemplify this habit. `@piximi/store`, for example, includes Redux actions for creating, updating, and deleting images that are used by multiple packages. Because each of these packages use the same `@piximi/store` actions, we can ensure the behavior between packages is consistent.

## Organization

This repository includes both the Piximi web app \(`packages/piximi`\) and the handful of discrete @piximi sub-packages \(`packages/@piximi/*`\) written concurrently or alongside the web app. The packages included in the packages directory are versioned together and simultaneously published to the NPM package repository.

#### @piximi/components

Generic React components

#### @piximi/evaluate-classifier-dialog

Piximi’s `EvaluateClassifierDialog` component

#### @piximi/fit-classifier-dialog

Piximi’s `FitClassifierDialog` component

#### @piximi/gallery-dialog

Piximi’s `GalleryDialog` component

#### @piximi/help-dialog

Piximi’s `HelpDialog` component

#### @piximi/hooks

Generic React hooks

#### @piximi/image-viewer-dialog

Piximi’s `ImageViewerDialog` component

#### @piximi/models

Piximi’s TensorFlow.js models

#### @piximi/navigation-drawer

Piximi’s `NavigationDrawer` component

#### @piximi/open-example-classifier-dialog

Piximi’s `OpenExampleClassifierDialog` component

#### @piximi/send-feedback-dialog

Piximi’s `SendFeedbackDialog` component

#### @piximi/settings-dialog

Piximi’s `SettingsDialog` component

#### @piximi/store

Piximi’s Redux actions, reducers, selectors, and stores

#### @piximi/theme

Piximi’s Material UI theme

#### @piximi/translations

Piximi’s translations

#### @piximi/types

Piximi’s generic TypeScript definitions

#### @piximi/upload-image-dialog

Piximi’s `UploadImageDialog` component

#### piximi

The piximi web app

## Working on a package

Maybe you just experienced a bug or you want to add a feature to Piximi. 

Within a package we use [storybook](https://storybook.js.org/) to work on UI components 

```
yarn storybook
```

## Creating a new package

#### Storybook

Packages with React components should include a `storybook` command and a `.storybook` directory with an appropriate Storybook configuration.

Most packages will only have one story that corresponds to the package’s one exported component. For example, `image-viewer-dialog` has one story for the `ImageViewerDialog` component. Likewise, `fit-classifier-dialog` has one story for the `FitClassifierDialog` component. A noteworthy exception are packages that export more than one component, e.g. `@piximi/components` has a story for each of its exported components.

{% hint style="info" %}
Please report all errors or issues you encounter in our tutorial to [https://github.com/piximi/piximi-issues](https://github.com/piximi/piximi-issues)
{% endhint %}



