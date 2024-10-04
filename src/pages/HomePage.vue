<template>
  <div class="container">
    <TitleAuthor />

    <main class="container main">
      <Controls
        :visibility="visibility"
        @toggleVisibility="toggleVisibility"
        class="main__controls"
      />

      <Poem :visibility="visibility" class="main__poem" />

      <div class="main__block"></div>
    </main>
  </div>
</template>

<script>
import TitleAuthor from "@/components/TitleAuthor.vue";
import Controls from "@/components/Controls.vue";
import Poem from "@/components/Poem.vue";

export default {
  components: {
    TitleAuthor,
    Controls,
    Poem,
  },
  data() {
    return {
      visibility: [true, true, true, true],
    };
  },
  methods: {
    toggleVisibility(index) {
      const visibleCount = this.visibility.filter((v) => v).length;
      if (visibleCount === 1 && this.visibility[index]) {
        return;
      }
      this.visibility[index] = !this.visibility[index];
    },
  },
};
</script>

<style scoped lang="scss">
.container {
  margin: 0 auto;
  padding: 40px 0px;
  font-family: "Times New Roman", Times, serif;
  text-align: center;
}
.main {
  display: flex;
  justify-content: center;
  align-items: start;
  &__block {
    width: 33.333%;
  }
  &__poem {
    width: 33.333%;
  }
  &__controls {
    width: 33.333%;
  }
}
</style>
