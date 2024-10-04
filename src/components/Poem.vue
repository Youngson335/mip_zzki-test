<template>
  <div class="poem">
    <p v-if="visibility[0]">
      Out of the night that covers me,<br />
      Black as the pit from pole to pole,<br />
      I thank whatever gods may be<br />
      For my unconquerable soul.
    </p>

    <p v-if="visibility[1]">
      In the fell clutch of circumstance<br />
      I have not winced nor cried aloud.<br />
      Under the bludgeonings of chance<br />
      My head is bloody, but unbowed.
    </p>

    <p v-if="visibility[2]">
      Beyond this place of wrath and tears<br />
      Looms but the Horror of the shade,<br />
      And yet the menace of the years<br />
      Finds and shall find me unafraid.
    </p>

    <p v-if="visibility[3]">
      It matters not how strait the gate,<br />
      How charged with punishments the scroll,<br />
      I am the master of my fate,<br />
      I am the captain of my soul.
    </p>
  </div>
</template>

<script>
export default {
  name: "Poem",
  props: {
    visibility: Array,
  },
};
</script>

<style scoped>
.poem p {
  margin-bottom: 1.5em;
  line-height: 1;
  font-size: 3vw;
}
</style>
