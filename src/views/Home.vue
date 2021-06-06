<template>
  <div class="box">
    <!-- <div class="left"></div>
    <div class="middle">
      <div class="handleToPage1CLick" @click="handleToPage1CLick">
        this is home
      </div>
    </div>
    <div class="right"></div> -->
    <div class="tabWrapper">
      <div
        @click="handleTabClick(item)"
        v-for="(item, index) in list"
        :key="index"
      >
        {{ item.name }}
      </div>
    </div>
    <keep-alive>
      <component :is="active"></component>
    </keep-alive>
  </div>
</template>

<script>
import Page1 from "./page1";
import Page2 from "./page2";

export default {
  name: "Home",
  props: {},
  data() {
    return {
      active: "Page1",
      list: [
        {
          name: "Page1",
        },
        {
          name: "Page2",
        },
      ],
    };
  },
  components: { Page1, Page2 },
  methods: {
    handleToPage1CLick() {
      this.$router.push({
        path: "/page1",
      });
    },
    handleTabClick(item) {
      this.active = item.name;
    },
  },
  mounted() {
    console.log("home");
  },
  computed: {},
  watch: {},
};
</script>

<style lang="scss" scoped>
.box {
  width: 100%;
  height: 100% !important;
  background: skyblue;
  /* & div:nth-child(1) {
    width: 300px;
    padding: 50px;
    background: slateblue;
    box-sizing: border-box;
  }
  & div:nth-child(2) {
    padding: 50px;
    width: 300px;
    background: springgreen;
  }
  & div:nth-child(3) {
    width: 300px;s
    background: tan;
  } */
  .tabWrapper {
    display: flex;
    height: 100%;
    & div:nth-child(1) {
      flex: 1;
      line-height: 400px;
      text-align: center;
      background: skyblue;
    }
    & div:nth-child(2) {
      flex: 1;
      line-height: 400px;
      text-align: center;
      background: yellowgreen;
    }
  }
}
</style>
