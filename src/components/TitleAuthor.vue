<template>
  <div class="poem__info">
    <div class="info__block"></div>
    <div class="info__title">
      <h1 class="info__title--h1">Invictus</h1>
    </div>
    <div class="info__author">
      <p class="info__author--p">By William Ernest Henley</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "TitleAuthor",
};
</script>

<style scoped lang="scss">
.poem__info {
  display: flex;
  align-items: center;
  width: 100%;
  text-align: center;
  justify-content: space-between;
  margin-bottom: 20px;
}

.info {
  &__title {
    margin: 0 auto;
    width: 33.333%;
    &--h1 {
      font-size: 6vw;
      margin: 0;
    }
  }
  &__block {
    margin: 0 auto;
    width: 33.333%;
  }

  &__author {
    width: 33.333%;
    &--p {
      font-size: 3vw;
      font-style: italic;
    }
  }
}
</style>
