<template>
  <div id="app">
    <h1>vue-nani-spinner</h1>
    <h3>Spinner that is simple as a single celled organisms</h3>
    <hr>

    <h4>Install</h4>
    <p class="code">npm install vue-nani-spinner --save</p>

    <h4>Use</h4>
    <p class="code">@import '~vue-nani-spinner/dist/index.css';
      <br>...
      <br>import Spinner from 'vue-nani-spinner'
      <br>...
      <br>components: {
      <br>&nbsp;&nbsp;Spinner
      <br>}
    </p>

    <h4>Properties</h4>
    <table class="code">
      <thead>
        <tr>
          <th>property</th>
          <th>type</th>
          <th>default</th>
          <th>description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>lineBackground</td>
          <td>String</td>
          <td>#EEEEEE</td>
          <td>line background color</td>
        </tr>
        <tr>
          <td>lineColor</td>
          <td>String</td>
          <td>#2196F3</td>
          <td>line color</td>
        </tr>
        <tr>
          <td>lineSize</td>
          <td>Number</td>
          <td>3</td>
          <td>line size (width)</td>
        </tr>
        <tr>
          <td>size</td>
          <td>Number</td>
          <td>32</td>
          <td>total size of spinner</td>
        </tr>
        <tr>
          <td>speed</td>
          <td>Number</td>
          <td>0.2</td>
          <td>speed of rotating</td>
        </tr>
        <tr>
          <td>text</td>
          <td>String</td>
          <td>''</td>
          <td>text message</td>
        </tr>
        <tr>
          <td>textColor</td>
          <td>String</td>
          <td>#555555</td>
          <td>text font color</td>
        </tr>
        <tr>
          <td>textSize</td>
          <td>Number | String</td>
          <td>''</td>
          <td>text font size, number in px or number with unit</td>
        </tr>
        <tr>
          <td>textSpacing</td>
          <td>Number</td>
          <td>4</td>
          <td>spacing</td>
        </tr>
      </tbody>
    </table>
    <br>
    <h4>Examples</h4>
    <vue-nani-spinner text="nani?"></vue-nani-spinner>
    <p class="code">&lt;vue-nani-spinner text=&quot;nani?&quot;&gt;&lt;/vue-nani-spinner&gt;</p>
    <vue-nani-spinner
      :size="40"
      :line-size="30"
      :speed="3.0"
      line-color="#FF0000"
      line-background="#FCC6E2"
      :direction="-1"
    ></vue-nani-spinner>
    <p class="code">
      &lt;vue-nani-spinner
      :size=&quot;40&quot;
      :line-size=&quot;30&quot;
      :speed=&quot;3.0&quot;
      line-color=&quot;#FF0000&quot;
      line-background=&quot;#FCC6E2&quot;
      :direction=&quot;-1&quot;
      &gt;&lt;/vue-nani-spinner&gt;
    </p>
    <h4>
      Check
      <a href="https://github.com/goto10hq/vue-nani-spinner">GitHub</a> for more
    </h4>
    <br>
  </div>
</template>

<script>
  import Vue from 'vue'
  //require("../dist/index.css");
  import VueNaniSpinner from '../src/index.js'

  export default {
    name: 'app',
    data: () => ({}),
    components: {
      VueNaniSpinner
    }
  }
</script>

<style>
  @import url("https://fonts.googleapis.com/css?family=Roboto:300,400,500,700,900");
  @import url("https://fonts.googleapis.com/css?family=Overpass+Mono:400,700");
  body {
    background-color: #fafafa;
  }
  #app {
    max-width: 980px;
    margin: auto;
    font-family: "Roboto", sans-serif;
    color: #2c3e50;
  }
  input {
    margin: 12px 0;
    font-family: inherit;
    font-size: inherit;
    padding: 8px 16px;
    border: none;
    border-bottom: 2px solid #4fc08d;
    outline: none;
    margin-right: 24px;
  }
  hr {
    border: none;
    border-bottom: 2px solid #ddd;
  }
  h1 {
    font-size: 48px;
    margin: 48px 0 8px 0;
    font-weight: 900;
  }
  h3 {
    margin: 0 0 24px;
    font-weight: 300;
  }
  h4 {
    margin: 36px 0 12px;
  }
  span {
    opacity: 0.5;
    margin-left: 16px;
    white-space: nowrap;
  }
  .code {
    padding: 24px;
    font-family: "Overpass Mono", monospace;
    background-color: #eee;
    font-size: 0.95em;
    font-weight: 500;
    line-height: 1.5em;
  }
  table.code {
    width: 100%;
    text-align: left;
  }
  table.code tbody tr {
    width: 100%;
    text-align: left;
    vertical-align: top;
  }
</style>