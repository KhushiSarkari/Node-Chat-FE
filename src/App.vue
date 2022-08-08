<script setup lang="ts">
import Participants from "./components/Participants.vue";
import Chat from "./components/Chat.vue";
</script>

<template>
  <div class="container">
    <Participants />
    <Chat />
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}
body {
  background: #c5ddeb;
  font: 14px/20px "Lato", Arial, sans-serif;
  padding: 40px 0;
  color: white;
}
.container {
  margin: 0 auto;
  width: 750px;
  background: #444753;
  border-radius: 5px;
}
.container:after {
  content: "";
  display: table;
  clear: both;
}
.column {
  float: left;
  padding: 2px;
}
.clearfix:after {
  visibility: hidden;
  display: block;
  font-size: 0;
  content: " ";
  clear: both;
  height: 0;
}
ul {
  list-style-type: none;
  padding: 20px;
  height: 770px;
}
li {
  padding-bottom: 20px;
}
li img {
  float: left;
}
.online,
.offline {
  margin-right: 3px;
  font-size: 10px;
}
.online {
  color: #86bb71;
}
.offline {
  color: #e38968;
}
</style>
