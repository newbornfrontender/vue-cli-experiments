<script>
import NavList from '@/components/NavList';

export default {
  name: 'App',
  components: {
    NavList,
  },
};
</script>

<template>
  <section>
    <header>
      <NavList />
    </header>

    <main>
      <router-view></router-view>
    </main>
  </section>
</template>
