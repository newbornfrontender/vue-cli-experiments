<script>
export default {
  name: 'List',
  props: {
    tag: {
      type: String,
      required: true,
      validator: (value) => {
        const ol = value === 'ol';
        const ul = value === 'ul';
        return ol || ul;
      },
    },
    items: {
      type: Array,
      required: true,
    },
  },
  render(h) {
    return h(
      this.tag,
      this.items.map((item) => {
        return h('li', [
          h(
            'router-link',
            {
              attrs: {
                to: item.path,
              },
            },
            item.title,
          ),
        ]);
      }),
    );
  },
};
</script>
