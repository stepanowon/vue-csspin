# vue-csspin
Spinner Component for Vue.js 3.x.
This project is an wrapper of [CSSPIN](https://www.npmjs.com/package/csspin)

[![npm](https://img.shields.io/npm/v/vue-csspin.svg )](https://www.npmjs.com/package/vue-csspin)
[![npm](https://img.shields.io/npm/dm/vue-csspin.svg)](https://www.npmjs.com/package/vue-csspin)
[![GitHub stars](https://img.shields.io/github/stars/stepanowon/vue-csspin.svg?style=social&label=Stars&style=for-the-badge)](https://github.com/stepanowon/vue-csspin/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/stepanowon/vue-csspin.svg?style=social&label=Fork&style=for-the-badge)](https://github.com/stepanowon/vue-csspin/network)
[![Build Status](https://travis-ci.org/stepanowon/vue-csspin.svg?branch=master)](https://travis-ci.org/stepanowon/vue-csspin)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)]()

------------

> Author : Stephen Won(원형섭), OpenSG Inc.        
> Online Demo2 : https://vue-csspin.vercel.app/

## License
MIT 
## Usage  

#### CDN - usage
~~~
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>vue-csspin 테스트</title>
<link rel="stylesheet" href="https://unpkg.com/vue-csspin/dist/vue-csspin.css" />
</head>
<body>
    <div id="app">
        <h2>VueCsspin Test</h2><hr />
        Loading Message : <input type="text" v-model="message" /><br />
        Spinner Style : 
        <select v-model="spinStyle">
            <option>cp-round</option>
            <option>cp-pinwheel</option>
            <option>cp-balls</option>
            <option>cp-bubble</option>
            <option>cp-flip</option>
            <option>cp-hue</option>
            <option>cp-skeleton</option>
            <option>cp-eclipse</option>
            <option>cp-boxes</option>
            <option>cp-morph</option>
            <option>cp-heart</option>
            <option>cp-meter</option>
        </select><br />
        <button @click="viewVueCsspin">Test Component</button>
        <vue-csspin v-if="visible" :message="message" :spin-style="spinStyle" />
    </div>
    <script src="https://unpkg.com/vue@next"></script>
    <script type="text/javascript" src="https://unpkg.com/vue-csspin"></script>
    <script type="text/javascript">
    var app = Vue.createApp({
        name: 'App',
        data() {
            return { 
            visible: false,
            message: "Loading",
            spinStyle : "cp-round"
            };
        },
        methods : {
            viewVueCsspin() {
                this.visible = true;
                setTimeout(()=>{
                    this.visible = false;
                }, 3000)
            }
        }
    })
    VueCsspin.default(app)
    app.mount("#app")
    </script>
</body>
</html>
~~~
##

#### NPM - install
~~~
npm install --save vue-csspin
- or -
yarn add vue-csspin
~~~

#### NPM - usage
~~~
<template>
  <div>
    <h2>VueCsspin Test</h2><hr />
    Loading Message : <input type="text" v-model="message" /><br />
    Spinner Style : 
    <select v-model="spinStyle">
        <option>cp-round</option>
        <option>cp-pinwheel</option>
        <option>cp-balls</option>
        <option>cp-bubble</option>
        <option>cp-flip</option>
        <option>cp-hue</option>
        <option>cp-skeleton</option>
        <option>cp-eclipse</option>
        <option>cp-boxes</option>
        <option>cp-morph</option>
        <option>cp-heart</option>
        <option>cp-meter</option>
    </select><br />
    <button @click="viewVueCsspin">Test Component</button>
    <vue-csspin v-if="visible" :message="message" :spin-style="spinStyle" />
  </div>
</template>

<script>
import { VueCsspin } from 'vue-csspin';
import 'vue-csspin/dist/vue-csspin.css';

export default {
  name: 'App',
  components: {
    VueCsspin
  },
  data() {
    return { 
      visible: false,
      message: "Loading",
      spinStyle : "cp-round"
    };
  },
  methods : {
    viewVueCsspin() {
      this.visible = true;
      setTimeout(()=>{
        this.visible = false;
      }, 3000)
    }
  }
}
</script>
~~~
##
#### Props
   * message
      - type : String
      - Loading Message
      - Default : "Loading" 
   * spinStyle 
     - type : String
     - Spinner Style
     - default : "cp-round"
     - available value : "cp-round", "cp-pinwheel", "cp-bubble", "cp-flip", "cp-hue", "cp-skeleton", "cp-eclipse", "cp-boxes", "cp-morph", "cp-heart", "cp-meter"
     - about more detail style ---> https://webkul.github.io/csspin/

