<template>
  <div class="starred-modal">
    <div class="search-output">
      <ul class="output-list">
        <li v-if="starredBoards" v-for="board in starredBoards">
          <RouterLink @click="closeModal" :to="'/details/' + board._id">
            <div class="row">
              <div class="board-recent">
                <div v-if="board.style.backgroundImage" class="imgPreview"
                  :style="{ background: board.style.backgroundImage, 'background-size': 'cover', 'background-position': 'center' }">
                </div>
                <div v-else class="colorPreview" :style="{ background: board.style.backgroundColor }">
                </div>
                <div class="info">
                  <h2 class="board-title">{{ board.title }}</h2>
                  <p>{{loggedinUser.fullname}} work space</p>
                </div>
              </div>
              <div @click.stop.prevent="toggleStar(board)" class="btn-star" :class="boardClass"></div>
            </div>
          </RouterLink>
        </li>
        <div v-if="starredBoards.length === 0" class="empty-starred">
          <img src="../assets/styles/img/bg.svg" alt="" />
          <p>Star important boards to access them quickly and easily.</p>
        </div>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isFull: true,
    };
  },
  methods: {
    changeStar() {
      this.isFull = !this.isFull;
    },
    closeModal() {
      this.$emit("closeModal");
    },
    toggleStar(board) {
      board = JSON.parse(JSON.stringify(board));
      board.isStarred = !board.isStarred;
      this.$emit("star", board);
    },
  },
  computed: {
    starredBoards() {
      return this.$store.getters.starredBoards;
    },
    boardClass() {
      return {
        unstarred: !this.isFull,
        starred: this.isFull,
      };
    },
    loggedinUser() {
      return this.$store.getters.loggedinUser
    }

  },
};
</script>

<style></style>
