<template>
  <div>
    <div v-html="htmlContent"></div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {},
  data() {
    return {
      htmlContent: "",
    };
  },
  components: {},
  methods: {},
  mounted() {
    this.htmlContent = this.$converter.makeHtml("../assets/resume.md");
  },
  computed: {},
  watch: {},
};
</script>

<style lang="scss" scoped></style>
