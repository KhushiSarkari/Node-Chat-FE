<script setup lang="ts">
</script>

<template>
  <div class="column participants">
    <div class="search">
      <input type="text" placeholder="Search.." />
      <i class="fa fa-magnifying-glass"></i>
    </div>
    <ul class="participant-list">
      <li class="clearfix">
        <img
          src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/chat_avatar_01.jpg"
          alt="avatar"
        />
        <div class="info">
          <div class="name">Laura Chase</div>
          <div class="status">
            <i class="fa fa-circle offline"></i> left 5 min ago
          </div>
        </div>
      </li>

      <li class="clearfix">
        <img
          src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/chat_avatar_01.jpg"
          alt="avatar"
        />
        <div class="info">
          <div class="name">Jeremy Crawford</div>
          <div class="status"><i class="fa fa-circle online"></i> online</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.participants {
  width: 250px;
}
.search {
  padding: 20px;
}
input {
  border-radius: 3px;
  border: none;
  padding: 14px;
  color: white;
  background: #6a6c75;
  width: 90%;
  font-size: 14px;
}
.fa-magnifying-glass {
  position: relative;
  left: -25px;
}
.info {
  float: left;
  margin-top: 8px;
  padding-left: 8px;
}
.status {
  color: #92959e;
}
</style>
