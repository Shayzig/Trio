<template>
  <div class="recent-modal">
    <div class="search-output">
      <ul class="output-list">
        <li v-for="board in recentBoards">
          <RouterLink @click="closeModal" :to="'/details/' + board._id">
            <div class="row">
              <div v-if="board.style.backgroundImage" class="imgPreview"
                :style="{ background: board.style.backgroundImage, 'background-size': 'cover', 'background-position': 'center' }">
              </div>
              <div v-else class="colorPreview" :style="{ background: board.style.backgroundColor }">
              </div>
              <div class="text">
                <h2>{{ board.title }}</h2>
                <p>{{loggedinUser.fullname}} work space</p>
              </div>
            </div>
          </RouterLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  computed: {
    recentBoards() {
      return this.$store.getters.recentBoards;
    },
    loggedinUser() {
      return this.$store.getters.loggedinUser
    }
  },
  methods: {
    closeModal() {
      this.$emit('closeModal')
    }
  },
};
</script>

<style></style>
