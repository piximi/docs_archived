---
description: 'Run Piximi locally, the quick and easy way'
---

# Getting Started

## 1. Download the Repository

Get the latest master of Piximi from Github

```
git clone https://github.com/piximi/piximi
```

You successfully downloaded the newest branch of Piximi. Let's cd into it

```bash
cd ./piximi
```

## 2. Install all dependencies

Within the newly cloned repository run

```bash
yarn bootstrap
```

This will install all sub repositories which Piximi depend on. However, we still need to build a `dist` file for each package. This is done by running

```bash
yarn build
```

{% hint style="info" %}
Piximi consists of independent sub-repositories found in piximi/packages/@piximi, We use [lerna](https://github.com/lerna/lerna) to manage all dependencies.
{% endhint %}

## 3. Run Piximi locally

Almost done! Go to the packages/piximi folder

```bash
cd ./packages/piximi
```

Let's run a local version of the most up-to-date Piximi branch

```bash
yarn start
```

🎉 Congratulations! You should see the newest version of Piximi running locally at: [http://localhost:3000/](http://localhost:3000/)

{% hint style="info" %}
Please report any errors or issues you encounter in our tutorial to [https://github.com/piximi/piximi-issues](https://github.com/piximi/piximi-issues)
{% endhint %}

