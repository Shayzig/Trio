<template>
    <div class="board" @click="goToDetails()">
      <div class="drop">
        <div @click.stop.prevent="toggleStar" class="btn-star" :class="boardClass"></div>
        <h2>{{ board.title.toUpperCase() }}</h2>
      </div>
    </div>

  <!-- <button @click="removeBoard(board._id)">X</button> -->
</template>

<script>
export default {
  props: ["board"],

  data() {
    return {
    };
  },

  methods: {
    removeBoard(boardId) {
      this.$emit("remove", boardId);
    },
    toggleStar() {
      const board = JSON.parse(JSON.stringify(this.board));
      board.isStarred = !board.isStarred;
      this.$emit("star", board);
    },
    goToDetails() {
      const board = JSON.parse(JSON.stringify(this.board));
      board.isRecent = true;
      board.recentAt = Date.now();
      this.$emit("recent", board);
      this.$router.push(`/details/${this.board._id}`);
    },
  },
  computed: {
    imgUrl() {
      if (this.board.style.backgroundImage) {
        return `${this.board.style.backgroundImage}`;
      } else {
        return this.board.style.backgroundColor;
      }
    },
    boardClass() {
      return {
        unstarred: !this.board.isStarred,
        starred: this.board.isStarred,
      }
    },
  },
};
</script>

<style>
.board {
  background-image: v-bind(imgUrl);
  background-position: center;
  background-size: cover;
}
</style>
