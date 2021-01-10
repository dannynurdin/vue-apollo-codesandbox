<template>
  <div :key="post.id">
    <h3>{{ post.title }}</h3>
    <p>{{ post.content }}</p>
    <span>{{ post.date }}</span>
  </div>
</template>

<script>
export default {
  name: "PostItem",
  props: ["post"],
};
</script>