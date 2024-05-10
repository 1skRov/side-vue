<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>
<template>
  <div class="list">
    <div class="list-single">
      <!-- 1 -->
      <svg
        class="icon-move"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M8.5 7C9.60457 7 10.5 6.10457 10.5 5C10.5 3.89543 9.60457 3 8.5 3C7.39543 3 6.5 3.89543 6.5 5C6.5 6.10457 7.39543 7 8.5 7Z"
        />
        <path
          d="M15.5 7C16.6046 7 17.5 6.10457 17.5 5C17.5 3.89543 16.6046 3 15.5 3C14.3954 3 13.5 3.89543 13.5 5C13.5 6.10457 14.3954 7 15.5 7Z"
        />
        <path
          d="M10.5 12C10.5 13.1046 9.60457 14 8.5 14C7.39543 14 6.5 13.1046 6.5 12C6.5 10.8954 7.39543 10 8.5 10C9.60457 10 10.5 10.8954 10.5 12Z"
        />
        <path
          d="M15.5 14C16.6046 14 17.5 13.1046 17.5 12C17.5 10.8954 16.6046 10 15.5 10C14.3954 10 13.5 10.8954 13.5 12C13.5 13.1046 14.3954 14 15.5 14Z"
        />
        <path
          d="M10.5 19C10.5 20.1046 9.60457 21 8.5 21C7.39543 21 6.5 20.1046 6.5 19C6.5 17.8954 7.39543 17 8.5 17C9.60457 17 10.5 17.8954 10.5 19Z"
        />
        <path
          d="M15.5 21C16.6046 21 17.5 20.1046 17.5 19C17.5 17.8954 16.6046 17 15.5 17C14.3954 17 13.5 17.8954 13.5 19C13.5 20.1046 14.3954 21 15.5 21Z"
        />
      </svg>
      <!-- 2 -->
      <img :src="post.imageUrl" alt="img" class="w-4 mr-2">
      <p class="text-sm">{{ post.title }}</p>
    </div>
    <div class="count active_count">
      <p class="count-text">{{post.msg}}</p>
    </div>
  </div>
</template>
<style>
.list {
  @apply flex justify-between items-center py-1 cursor-pointer;
}
.list .list-single {
  @apply flex items-center p-2;
}
.icon-move {
  @apply w-4 fill-gray-400 mr-1.5;
}
.list .count {
  @apply bg-gray-200 rounded-md text-center w-5 h-5 mr-1.5;
}
.list .count .count-text {
  @apply text-xs font-semibold text-gray-600 py-0.5;
}
.active {
  @apply bg-gray-200 rounded;
}
.active .active_count {
  @apply bg-white;
}
</style>
