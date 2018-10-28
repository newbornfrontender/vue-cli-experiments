<script>
export default {
  name: 'PostPreview',
  props: {
    title: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    imageHeight: {
      type: Number,
      default: 150,
    },
    imageUrl: {
      type: String,
      required: true,
    },
    imagePosition: {
      type: String,
      default: 'center',
    },
    preview: {
      type: String,
      required: false,
    },
    tags: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<template>
  <article :class="$style.post">
    <h2 :class="$style.title">{{ title }}</h2>

    <div
      :class="$style.tagWrapper"
      v-if="tags.length"
    >
      <span
        :class="$style.tag"
        v-for="tag of tags"
        :key="tag"
      >
        {{ tag }}
      </span>
    </div>

    <figure :class="$style.imageWrapper">
      <figcaption :class="$style.imageLabel">{{ label }}</figcaption>

      <div
        :class="$style.image"
        :style="{
          height: `${imageHeight}px`,
          backgroundImage: `url(${imageUrl})`,
          backgroundPosition: imagePosition,
        }"
      />
    </figure>

    <p :class="$style.previewText">{{ preview }}</p>

    <p v-if="$slots.default">
      <slot />
    </p>
  </article>
</template>

<style module>
.post {
  background-color: #607d8b;
  border-radius: 20px;
  transform: scale(0.98);
  box-shadow: 0px 2px 3px #3d5561;
}

.post:not(:last-child) {
  margin-bottom: 12px;
  transition-duration: 0.2s;
}

.post:hover {
  transform: scale(1);
  box-shadow: 0px 3px 10px 1px #3d5561;
}

.title {
  margin: 0;
  padding: 10px 0;
  font-size: 30px;
  text-align: center;
  color: #30434c;
  text-shadow: 1px 1px #607d8b, 2px 2px #30434c;
}

.tagWrapper {
  display: flex;
  justify-content: flex-end;
  padding: 5px 0;
}

.tag {
  margin-right: 4px;
  padding: 2px;
  background-color: #9E9E9E;
  color: #47484c;
  border-radius: 3px;
  cursor: pointer;
}

.tag:hover {
  color: white;
}

.imageWrapper {
  position: relative;
  margin: 0;
  box-sizing: border-box;
}

.imageLabel {
  position: absolute;
  bottom: 0;
  width: 100%;
  padding: 2px 0;
  background-color: rgba(0, 0, 0, 0.4);
  color: white;
  text-align: center;
}

.image {
  width: 100%;
  background-size: 100%;
  cursor: pointer;
}

.previewText {
  margin: 0;
  padding: 10px;
  font-size: 16px;
  color: white;
}
</style>
