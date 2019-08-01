# Nuxt
vuejs on steroids
https://nuxtjs.org/
https://www.vuemastery.com/nuxt-cheat-sheet/


July 31, 2019
-------------

notes from Udemy Course / Max S.:
https://www.udemy.com/nuxtjs-vuejs-on-steroids/

## Creating a Nuxt App 

- CLI Command to create nuxt app: npx create-nuxt-app <app-name>
```bash
npx create-nuxt-app app-name
```
local git repo in the labs dir linked to github repo:
https://github.com/hr-labs/skills-nuxt-create-app

## Pages, Routing and Views

- From folders to routes: create files or folders in the page dir and nuxt will create automatically the equivalent routes/components
- Route with dynamic path via _file.vue - dynamic reference with {{ $route.params.id }}
```vue
<template>
    <h1>A single user, with ID: {{ $route.params.id }}</h1>
</template>
```
- or using a dynamic folder name in pages eg: _id and ensure there is an index.vue in the new folder
- the dynamic folder approach is needed for adding more files and/or further dynamic folders
