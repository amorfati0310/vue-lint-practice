<template>
  <header>
    <h1 :class="{ hide: isShow }">{{ title }}</h1>
    <button @click="toggleShowTitle">toggle show title</button>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
    };
  },
  props: {
    title: {
      type: String,
      default: '',
    },
  },
  methods: {
    toggleShowTitle() {
      this.isShow = !this.isShow;
    },
  },
};
</script>

<style>
.hide {
  display: none;
}
</style>
