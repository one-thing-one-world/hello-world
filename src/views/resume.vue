<template>
  <div>
    <my-markdown></my-markdown>
  </div>
</template>

<script>
import myMarkdown from "../assets/resume.md";
// import marked from "marked";

export default {
  name: "Resume",
  props: {},
  data() {
    return {
      // resume: require("../assets/resume.md"),
      // readme: this.md2html(resume),
    };
  },
  components: { myMarkdown },
  methods: {},
  mounted() {
    // this.htmlContent = this.$converter.makeHtml(resume);
  },
  computed: {},
  watch: {},
};
</script>

<style lang="scss" scoped></style>
