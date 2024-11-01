

<div align="center">

# Embedplay TikTok Vue

[![npm version](https://img.shields.io/npm/v/embedplay-tiktok-vue.svg?logo=npm&style=flat-square&label=Latest&color=blue)](https://www.npmjs.com/package/embedplay-tiktok-vue)
![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square)
![Package Size](https://img.shields.io/bundlephobia/minzip/embedplay-tiktok-vue?style=flat-square&color=yellow)
![Downloads](https://img.shields.io/npm/dt/embedplay-tiktok-vue.svg?style=flat-square&label=Downloads&color=orange)
[![License](https://img.shields.io/npm/l/embedplay-tiktok-vue.svg?style=flat-square&label=License&color=green)](https://github.com/demjhonsilver/embedplay-tiktok-vue/blob/main/LICENSE.md)






</div>




---------------------

## Table of Contents

- [Description](#description)
- [Release Notes](#release-notes)
- [Installation](#installation)
- [Paradigm](#paradigm)
- [License](#license)
- [Author](#author)

## Description

[Read the Documentation - TikTok Developers](https://developers.tiktok.com/doc/embed-player?enter_method=left_navigation)

This package provides a flexible and easy way to integrate TikTok videos into your Vue application with customizable display options.

This Vue component template is designed to embed a TikTok video player using the EmbedplayTikTokVue component. 

Framework | Supported versions
------ | -------- | 
![Vue.js](https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)  | 3 & above


-----

## Release-notes


Major Changes:

 v1.0.0
 - This Vue component renders a customizable TikTok player within an iframe, allowing users to embed TikTok posts directly into their applications. 

 - The component supports a flexible border radius, allowing you to easily adjust the corner curvature of the iframe to fit your design needs.


Patch Changes:

 v1.0.2
 - To emphasize the documentation for SFCs (single-file components), the Composition API, and the Options API.

 v1.0.1
 - Removed "webpack-env" from the "types" array in compilerOptions of tsconfig.json

___________

## Installation

To install the Embedplay TikTok Vue, you can use the following npm command:

```bash
npm install embedplay-tiktok-vue
```
------------
## Paradigm


Using Single-File Components (SFCs) - Composition API
---------
```js
<script setup>
import ExampleComponent  from 'example-component';
</script>
```

Example 1

```js
<script setup>
import EmbedplayTikTokVue  from 'embedplay-tiktok-vue';
</script>

<template>
  <div>
    <EmbedplayTikTokVue 
      postId="6718335390845095173" 
      :autoplay="false" 
      :controls="true" 
      :progressBar="true" 
      :playButton="true"
      :volumeControl="true" 
      :fullscreenButton="true" 
      :timestamp="true"
      :loop="false"
      :musicInfo="true"
      :description="false"
      :rel="true"
      :nativeContextMenu="false"
      :width="640" 
      :height="360"
    />
  </div>
</template>
```





----------------


Using Components (Options API)
---------
```js
<script>
import ExampleComponent  from 'example-component';
export default {
  components: {
    ExampleComponent
  }
};
</script>
```

Example 2


```js
<script>
import EmbedplayTikTokVue  from 'embedplay-tiktok-vue';
export default {
  components: {
    EmbedplayTikTokVue
  }
};
</script>

<template>
  <div>
    <EmbedplayTikTokVue 
      postId="6718335390845095173" 
      :autoplay="false" 
      :controls="true" 
      :progressBar="true" 
      :playButton="true"
      :volumeControl="true" 
      :fullscreenButton="true" 
      :timestamp="true"
      :loop="false"
      :musicInfo="true"
      :description="false"
      :rel="true"
      :nativeContextMenu="false"
      :width="640" 
      :height="360"
    />
  </div>
</template>
```
---------
You can also use a global declaration.(main.js)
---------

```js
import { createApp } from 'vue';
import App from './App.vue';
import EmbedplayTikTokVue from 'embedplay-tiktok-vue'; // Import global

createApp(App)
  .component('EmbedplayTikTokVue', EmbedplayTikTokVue) 
  .mount('#app');
```

If you choose global, you can use the code below:

```js
<template>
    <EmbedplayTikTokVue 
      postId="6718335390845095173" 
      :autoplay="false" 
      :controls="true" 
      :progressBar="true" 
      :playButton="true"
      :volumeControl="true" 
      :fullscreenButton="true" 
      :timestamp="true"
      :loop="false"
      :musicInfo="true"
      :description="false"
      :rel="true"
      :nativeContextMenu="false"
      :width="640" 
      :height="360"
    />
</template>
```


--------
Optional
--------

You can set any number for the border radius parameter:


```js
     :borderRadius="10" // You can set any number value.
```
Example:

```js
    <EmbedplayTikTokVue 
      postId="6718335390845095173" 
      :autoplay="false" 
      :controls="true" 
      :progressBar="true" 
      :playButton="true"
      :volumeControl="true" 
      :fullscreenButton="true" 
      :timestamp="true"
      :loop="false"
      :musicInfo="true"
      :description="false"
      :rel="true"
      :nativeContextMenu="false"
      :width="640" 
      :height="360"
      :borderRadius="10"
    />
```

If you don't want to apply a border radius, simply remove the parameter.
______________________________________________






## License

MIT

- This package is distributed under the MIT License, which permits free use, modification, and distribution of the software.


[Source: TikTok Developers ](https://developers.tiktok.com/doc/overview)
----------------------------------------------------
## Author

Demjhon Silver