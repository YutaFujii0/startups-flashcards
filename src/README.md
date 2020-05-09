# startups-flashcards

> Flashcards to know startups

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## Firebase setup

```bash
$ npm install -g firebase-tools

# login
$ firebase login

# initialize
$ firebase init

# deploy
$ firebase deploy

# make sure to build before deploy
$ npm run build
```

configuration file
```
{
  "hosting": {
    "public": ".nuxt", # target directory relative path
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],

    # add this object
    "rewrites": [ {
      "source": "/",
      "destination": "/dist/server/index.spa.html"
    } ]
  }
}
```


reference:
- https://qiita.com/saongtx7/items/d97ef5aec393e704fd3f

## Configuration

use sass

```bash
$ npm install --save-dev node-sass sass-loader
```

reference:



