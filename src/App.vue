<template>
  <div id="app">
    <the-header/>
    <the-navbar/>
    <router-view/>
    <the-content/>
  </div>
</template>

<script>

import theNavbar from './components/layout/theNavbar.vue'
import theHeader from './components/layout/theHeader.vue'
import theContent from './components/layout/theContent.vue'

export default {
  name: 'App',
  components: {
    theNavbar,
    theHeader,
    theContent
  }
  
}
</script>

<style>

@import url('style/base/button.css');
@import url('style/base/input.css');
@import url('style/base/table.css');
@import url('style/base/dialog.css');
@import url('style/base/icon.css');
@import url('style/base/combobox.css');


body {
    margin: 0;
}

.bg-primary {
    background-color: #01B075;
}


.text-align-center{
    text-align: center;
}

.text-align-right{
    text-align: right;
}

a{
    text-decoration: none;
    color: #000;;
    cursor: pointer;
}
body{
    font-family: GoogleSans-Regular;
    font-size: 13px;
}

@font-face {
    font-family: 'GoogleSans-Regular';
    src: url('assets/font/GoogleSans-Regular.otf') format('opentype');
}

@font-face {
    font-family: 'GoogleSans-Bold';
    src: url('assets/font/GoogleSans-Bold.otf') format('opentype');
}

@font-face {
    font-family: 'GoogleSans-Italic';
    src: url('assets/font/GoogleSans-Italic.otf') format('opentype');
}

@font-face {
    font-family: 'GoogleSans-BoldItalic';
    src: url('assets/font/GoogleSans-BoldItalic.otf') format('opentype');
}

.bg-selected-row{
    background-color: #f0f0f0;
}
</style>
