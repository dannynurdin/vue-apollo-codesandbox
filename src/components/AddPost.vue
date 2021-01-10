<template>
  <div>
    <form @submit="submit">
      <fieldset>
        <input type="text" placeholder="Title" v-model="title" /><br />
        <textarea type="text" placeholder="Text" v-model="text" /><br />
        <select>
          <option value="">Select</option>
        </select>
      </fieldset>
      <input class="btn btn-primary" type="submit" value="Send" />
    </form>
  </div>
</template>

<script>
export default {
  name: "AddPost",
  data() {
    return {
      title: "",
      text: "",
    };
  },
  methods: {
    submit(e) {
      e.preventDefault();
      alert(this.$data.title);
    },
  },
};
</script>