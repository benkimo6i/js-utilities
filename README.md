# js-utilities

Resource for common utility functions in vanilla js

## Build Setup

``` bash
# install dependencies
$ npm run install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## How To Add New/Your Own Functions
1. First create a new branch
2. Then find /components/UtilityLink.vue

   Add a new obj to links array with your name, a slug and a short title that describes what your function does

   Remember your id & title

3. Next find /pages/utilities/_id.vue

   Add a new obj to utilities array with your name, a description of the function, an id (this will be the slug that you used in the previous step), a title (this can be the title that you used in the previous step), a link to your github and an escaped string of your JavaScript code

   If you need help w/ your escaped string, I recommend this online tool: [https://www.freeformatter.com/json-escape.html](https://www.freeformatter.com/json-escape.html)

4. Submit PR to merge your branch into master! 


