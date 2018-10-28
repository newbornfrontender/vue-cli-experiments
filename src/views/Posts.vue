<script>
import PostPreview from '@/components/PostPreview';

export default {
  name: 'Posts',
  components: {
    PostPreview,
  },
  data: () => ({
    title: 'Posts',
    posts: [
      {
        title: 'How to write code',
        label: 'PHP code in Sublime Text',
        imageHeight: 200,
        imageUrl:
          'http://www.lumete.it/wp-content/uploads/2016/09/code-944499_960_720.jpg',
        tags: ['PHP', 'CSS', 'HTML', 'Code', 'Sublime Text 2', 'Introduction', 'Beginners'],
        preview: 'In this article I will tell you how to write code correctly',
      },
      {
        title: 'Test',
        label: 'Test',
        imageUrl:
          'http://www.lumete.it/wp-content/uploads/2016/09/code-944499_960_720.jpg',
        tags: ['Test'],
        preview: 'Test',
      },
    ],
  }),
};
</script>

<template>
  <div>
    <h1>{{ title }}</h1>

    <section>
      <PostPreview
        v-for="{ title, label, alt, imageHeight, imageUrl, preview, tags } of posts"
        :key="title"
        :title="title"
        :label="label"
        :imageHeight="imageHeight"
        :imageUrl="imageUrl"
        :preview="preview"
        :tags="tags"
      />
    </section>
  </div>
</template>
