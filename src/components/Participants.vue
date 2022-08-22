<script setup lang="ts">
import { onMounted, ref } from "vue";

const participants = ref([] as any);
const loggedInUser = ref("allan@yopmail.com");
const selectedRecipient = ref("");
const emit = defineEmits(["switchConversation"]);

const getParticipantsData = () => {
  fetch("http://localhost:3000/user")
    .then((res) => res.json())
    .then((data) => {
      participants.value = data;
    });
};

const switchConversation = (participant: string) => {
 emit("switchConversation", participant);
};

onMounted(() => {
  getParticipantsData();
});
</script>

<template>
  <div class="column participants">
    <div class="search">
      <input type="text" placeholder="Search.." />
      <i class="fa fa-magnifying-glass"></i>
    </div>
    <ul class="participant-list">
      <!-- <li class="clearfix">
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
      </li> -->

      <li
        class="clearfix"
        v-for="participant in participants"
        :key="participant._id"
        @click="switchConversation(participant.email)"
      >
        <template v-if="participant.email !== loggedInUser">
          <img
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/chat_avatar_01.jpg"
            alt="avatar"
          />
          <div class="info">
            <div class="name">
              {{ participant.firstName }} {{ participant.lastName }}
            </div>
            <!-- <div class="status"><i class="fa fa-circle online"></i> online</div> -->
          </div>
        </template>
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
