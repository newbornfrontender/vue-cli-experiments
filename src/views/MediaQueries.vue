<script>
import Media from 'vue-media';

export default {
  name: 'MediaQueries',
  components: {
    Media,
  },
  data: () => ({
    visible: true,
  }),
  methods: {
    mediaEnter() {
      this.visible = true;
    },
    mediaLeave() {
      this.visible = false;
    },
  },
};
</script>

<template>
  <section>
    <h1>Media Queries</h1>

    <p>This is media queries page</p>

    <p v-if="visible">I am visible</p>
    <p v-else>I am not visible</p>

    <div>
      <p>
        <media
          :query="'(min-width: 768px)'"
          @media-enter="mediaEnter"
          @media-leave="mediaLeave"
        >Bigger than 768</media>
        <media :query="'(max-width: 768px)'">Smaller than 768</media>
      </p>
    </div>
  </section>
</template>
