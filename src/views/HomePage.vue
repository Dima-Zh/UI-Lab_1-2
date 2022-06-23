<template>
  <div class="container">
    <div v-if="$store.state.currentUser">
      <router-link
        to="/create-question"
        custom
        v-slot="{ navigate, isActive, isExactActive }"
      >
        <button
          id="create-question-btn"
          role="link"
          class="btn btn-primary mb-3"
          @click="navigate"
          :class="{ active: isActive, 'exact-active': isExactActive }"
        >
          Create new polling
        </button>
      </router-link>
    </div>
    <div v-else>
      <div class="alert alert-warning" role="alert">
        You must first register in order to be able to participate in the survey
        and ask questions yourself.
      </div>
    </div>
    <QuestionList :questions="$store.state.questions.questionList" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import QuestionList from "@/components/QuestionList.vue";

export default defineComponent({
  name: "HomePage",
  components: { QuestionList },
});
</script>
