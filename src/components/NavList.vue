<script>
import List from './List';

export default {
  name: 'NavList',
  components: {
    List,
  },
  data: () => ({
    items: [
      {
        title: 'Home',
        path: '/',
      },
      {
        title: 'About',
        path: '/about',
      },
      {
        title: 'Posts',
        path: '/posts',
      },
      {
        title: 'Media Queries',
        path: '/media-queries',
      },
    ],
  }),
};
</script>

<template>
  <nav>
    <List
      :tag="'ul'"
      :items="items"
    />
  </nav>
</template>
