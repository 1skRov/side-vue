<script>
  import CreateNewList from "./CreateNewList.vue";
  import SidePrivateList from "./SidePrivateList.vue";
  export default {
    components: { CreateNewList, SidePrivateList },
    props: {
      posts: {
        type: Array,
        required: true,
      },
    },
  };
</script>

<template>
  <div class="main-text mb-6">
    <p>Private</p>
    <!-- home -->
    <side-private-list v-for="post in posts" :post="post" />
    <!-- create -->
    <CreateNewList />
  </div>
</template>


<style>
  .main-text > p {
    @apply text-lg font-semibold mb-4;
  }
</style>
