<p align="center">
  <img src="./packages/docs/static/preview.png" alt="nuxt-firebase logo">
</p>

[![](https://david-dm.org/nuxt-community/firebase-module/status.svg?style=flat-square)](https://david-dm.org/nuxt-community/i18n-module)
[![](https://snyk.io/test/github/nuxt-community/firebase-module/badge.svg?style=flat-square)](https://snyk.io/test/github/nuxt-community/firebase-module)
[![](https://img.shields.io/npm/v/@nuxtjs/firebase/latest.svg?style=flat-square)](https://npmjs.com/package/@nuxtjs/firebase)
[![](https://img.shields.io/npm/dt/@nuxtjs/firebase.svg?style=flat-square)](https://npmjs.com/package/@nuxtjs/firebase)

> Easily integrate Firebase into your Nuxt project.

## IMPORTANT!

> ### ⚠️ **Nuxt 3 not supported ⚠️**:
>
> This module was written for Nuxt 2 and does currently not support Nuxt 3.
> There are currently no plans to support Nuxt 3 in the near future in this module.
> However, you can take a look at [VueFire Nuxt module for Nuxt 3 support](https://vuefire.vuejs.org/nuxt/getting-started.html)

> ### ℹ️ **Modular Mode (Firebase v9+) ℹ️**:
>
> This module does not support the new modular syntax from Firebase v9+.
>
> If you plan to use the new modular mode of Version 9, we advise you to implement Firebase manually as described in the following [medium article](https://lupas.medium.com/firebase-9-beta-nuxt-js-981cf3dac910).
>
> It is currently unclear when, and if, this module will support the new modular mode. See [discussion](https://github.com/nuxt-community/firebase-module/issues/597).

## Links

- 📘 [Documentation](https://firebase.nuxtjs.org/)
- 🔖 [Release notes](https://github.com/nuxt-community/firebase-module/releases)
- 👥 [Community](https://discord.nuxtjs.org/)

## Quick Setup

Make sure you are using the newest version of Nuxt and have Firebase >8.0.0 installed in your project.

```bash
yarn add firebase # OR npm i firebase
```

Install the module via NPM or Yarn:

```bash
yarn add @nuxtjs/firebase # OR npm i @nuxtjs/firebase
```

## Quick Config

Add the following to your nuxt.config.js.

See all configuration options [here](https://firebase.nuxtjs.org/guide/options/).

```js
modules: [
    [
      '@nuxtjs/firebase',
      {
        config: {
          apiKey: '<apiKey>',
          authDomain: '<authDomain>',
          projectId: '<projectId>',
          storageBucket: '<storageBucket>',
          messagingSenderId: '<messagingSenderId>',
          appId: '<appId>',
          measurementId: '<measurementId>'
        },
        services: {
          auth: true // Just as example. Can be any other service.
        }
      }
    ]
  ],
```

## Quick Usage

Now you can use all Firebase services with `this.$fire.auth`, `this.$fire.firestore`, `this.$fire.messaging` etc. (see list [here](https://firebase.nuxtjs.org/guide/usage/)).

Example:

```js
try {
  await this.$fire.auth.createUserWithEmailAndPassword("foo@foo.foo", "test");
} catch (e) {
  handleError(e);
}
```

## Guidelines for issues & feature requests

- Use the GitHub issue search — check if the issue or feature request has already been reported.
- Check if the issue has been fixed — try to reproduce it using the latest master or development branch in the repository.
- Isolate the problem — create a reduced test case and a live example.

A good issue shouldn't leave others needing to chase you up for more information. Please **try to be as detailed as possible** in your report. What is your environment? What steps will reproduce the issue? What versions are you using? What would you expect to be the outcome? All these details will help people to fix any potential bugs.

If you have difficulties that are most likely not bugs or if you just have a simple questions, please ask them in the [Nuxt Discord server](https://discord.nuxtjs.org) instead.

If you're issue does not suffice these guidelinses, it migt be closed immediately.

## License

MIT - [Nuxt-Community](https://github.com/nuxt-community) - [Pascal Luther](https://github.com/lupas)
