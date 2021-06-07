<template>
  <div class="markdown-body">
    <my-markdown></my-markdown>
    <!-- <div id="content"></div> -->
    <!-- <v-md-preview :text="text"></v-md-preview> -->
  </div>
</template>

<script>
import myMarkdown from "../assets/resume.md";

export default {
  name: "Resume",
  props: {},
  data() {
    return {};
  },
  components: { myMarkdown },
  methods: {},
  mounted() {},
  computed: {},
  watch: {},
};
</script>

<style lang="scss" scoped></style>
