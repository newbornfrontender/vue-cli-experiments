<script>
export default {
  name: 'About',
};
</script>

<template>
  <section>
    <h1 :class="$style.title">About</h1>

    <p>This is <span>About</span> page</p>
    <p>
      <vue-router to="/">Go to <span>Home</span></vue-router>
    </p>
  </section>
</template>

<style module>
.title {
  color: blue;
}
</style>
