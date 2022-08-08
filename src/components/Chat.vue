<script setup lang="ts">
</script>

<template>
  <div class="column chat">
    <div class="chat-header clearfix">
      <img
        src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/chat_avatar_01_green.jpg"
        alt="avatar"
      />

      <div class="chat-about">
        <div class="chat-with">Vincent Porter</div>
      </div>
    </div>
    <div class="messages">
      <ul>
        <li class="clearfix">
          <div class="message-data align-right">
            <span class="message-data-time">10:10 AM</span> &nbsp; &nbsp;
          </div>
          <div class="message other-message float-right">
            Hi Vincent, how are you? How is the project coming along?
          </div>
        </li>

        <li>
          <div class="message-data">
            <span class="message-data-time">10:12 AM</span>
          </div>
          <div class="message my-message">
            Are we meeting today? Project has been already finished and I have
            results to show you.
          </div>
        </li>
      </ul>
    </div>
    <div class="chat-message clearfix">
      <textarea
        name="message-to-send"
        id="message-to-send"
        placeholder="Type your message"
        rows="3"
      ></textarea>

      <button>Send</button>
    </div>
  </div>
</template>

<style scoped>
.chat {
  width: 500px;
  background: #f2f5f8;
  float: left;
  background: #f2f5f8;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  color: #434651;
}
.chat-header {
  padding: 20px;
  border-bottom: 2px solid white;
}
.chat-header img {
  float: left;
}

.chat-about {
  float: left;
  padding-left: 10px;
  margin-top: 15px;
}

.chat-with {
  font-weight: bold;
  font-size: 16px;
}

.messages {
  padding: 30px 30px 20px;
  border-bottom: 2px solid white;
  overflow-y: scroll;
}
.message-data {
  margin-bottom: 15px;
}

.message-data-time {
  color: lighten(#92959e, 8%);
  padding-left: 6px;
}

.message {
  color: white;
  padding: 18px 20px;
  line-height: 26px;
  font-size: 16px;
  border-radius: 7px;
  margin-bottom: 30px;
  width: 90%;
  position: relative;
}
.message:after {
  bottom: 100%;
  left: 7%;
  border: solid transparent;
  content: " ";
  height: 0;
  width: 0;
  position: absolute;
  pointer-events: none;
  border-bottom-color: #86bb71;
  border-width: 10px;
  margin-left: -10px;
}

.my-message {
  background: #86bb71;
}

.other-message {
  background: #94c2ed;
}
.other-message:after {
  border-bottom-color: #94c2ed;
  left: 93%;
}
.align-left {
  text-align: left;
}

.align-right {
  text-align: right;
}

.float-right {
  float: right;
}
.chat-message {
  padding: 30px;
}
.chat-message textarea {
  width: 100%;
  border: none;
  padding: 10px 20px;
  font: 14px/22px "Lato", Arial, sans-serif;
  margin-bottom: 10px;
  border-radius: 5px;
  resize: none;
}

.chat-message button {
  float: right;
  color: #94c2ed;
  font-size: 16px;
  text-transform: uppercase;
  border: none;
  cursor: pointer;
  font-weight: bold;
  background: #f2f5f8;
}
.chat-message button:hover {
  color: darken(#94c2ed, 7%);
}
</style>