<script setup>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";
import Timestamp from "./Timestamp.vue";
defineProps({
  tweet: Object,
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :name="tweet.user.name" :handle="tweet.user.handle" />
        <Timestamp :timestamp="tweet.timestamp" />
      </div>

      <Message :message="tweet.message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
