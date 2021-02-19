<template>
  <div class="post">
    <router-link :to="{ name: 'Details', params: { id: title } }">
      <h3>{{ post.title }}</h3>
    </router-link>
    <p>{{ snippet }}</p>
    <span v-for="tag in post.tags" :key="tag"> #{{ tag }} </span>
  </div>
</template>

<script>
import { computed } from "vue";
export default {
  props: ["post"],
  setup(props) {
    const snippet = computed(() => {
      return props.post.body.substring(0, 100) + "....";
    });

    const title = computed(() => {
      return (
        props.post.title.toLowerCase().split(" ").join("-") +
        "&id=" +
        props.post.id
      );
    });

    return { snippet, title };
  },
};
</script>

<style>
.post {
  background: #eee;
  border: 1px solid #333;
  margin: 20px auto;
  border-radius: 20px;
}

.post a {
  color: #333;
  text-decoration: none;
}
</style>