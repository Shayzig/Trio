<template>
  <div class="homepage">
    <div class="main-layout">
      <div class="demo">
        <h2>
          Trio brings all your <br />
          tasks, teammates, and <br />
          tools together
        </h2>
        <h6>
          Keep everything in the same place even if your team <br />
          isn’t.
        </h6>
        <RouterLink to="/board">
          <button>Let's Trio</button>
        </RouterLink>
      </div>

      <div class="right-hero-container">
        <img
          src="https://images.ctfassets.net/rz1oowkt5gyp/75rDABL8fyMtNLlUAtBxrg/c5e145977a86c41c47e17c69410c64f7/TrelloUICollage_4x.png?w=2280&fm=webp"
          alt=""
        />
      </div>

      <div class="wave">
        <img
          class="wave"
          src="../assets/styles/img/white-wave-mobile.svg"
          alt=""
        />
      </div>

      <div class="buttom-layout">
        <h4 class="trio">TRIO 101</h4>
        <div class="sub-header">
          <h1>A productivity powerhouse</h1>
          <h5>
            Simple, flexible, and powerful. All it takes are boards, lists, and
            <br />
            cards to get a clear view of who`s doing what and what needs to
            <br />
            get done. Learn more in our guide for getting started.
          </h5>
        </div>

        <div class="cards-container">
          <div class="card-1">
            <h5>Boards</h5>
            <p>
              Trio boards keep tasks organized and work moving forward. In a
              glance, see everything from “things to do” to “aww yeah, we did
              it!”
            </p>
          </div>
          <div class="card-2">
            <h5>Lists</h5>
            <p>
              The different stages of a task. Start as simple as To Do, Doing or
              Done—or build a workflow custom fit to your team’s needs. There’s
              no wrong way to Trio.
            </p>
          </div>
          <div class="card-3">
            <h5>Cards</h5>
            <p>
              Cards represent tasks and ideas and hold all the information to
              get the job done. As you make progress, move cards across lists to
              show their status.
            </p>
          </div>

          <img
            src="https://images.ctfassets.net/rz1oowkt5gyp/4U0VUZYX2tQmB5KVGxBabp/7321ac088fe8ec39dbe3069c47d7df99/Carousel_Image_Lists_2x.png?w=1140&fm=webp"
            alt=""
          />
        </div>
      </div>
    </div>
  </div>
  <div class="bg"></div>
</template>

<script>
import HomeHeader from "../cmps/HomeHeader.vue";
export default {
  name: "home",
  data() {
    return {};
  },
  computed: {},
  created() {},
  methods: {},
  components: {
    HomeHeader,
  },
};
</script>
