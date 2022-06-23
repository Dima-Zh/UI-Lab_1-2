<template>
  <h1>About Web-Site "Question"</h1>
  <img alt="logo-image" src="../assets/logo.jpg" class="rounded mb-3" />
  <p>This site was created for the opportunity to conduct surveys.</p>
  <p>It was created by Zhovnirskyi Dmytro KV-11mp</p>
  <p>
    This site was created for the opportunity to conduct a survey and looks like
    a question with predefined answers. Only registered users can create polls
    and respond.
  </p>
  <p>
    This site can be used to collect statistics on the things you need, for work
    or just for the sake of interest. Only the site administrator can delete the
    question.
  </p>
  <p>Admin user has possibility to see all users and delete any polling</p>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "AboutPage",
});
</script>
