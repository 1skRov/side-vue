<script>
import SideHead from "./components/SideHead.vue";
import SideBodyPrivate from "./components/SideBodyPrivate.vue";
import SideBodyWorkspace from "./components/SideBodyWorkspace.vue";
export default {
  components: {
    SideHead,
    SideBodyPrivate,
    SideBodyWorkspace,
  },
  data() {
    return {
      posts: [
        { id: 1, imageUrl: "/icons/home-house-svgrepo-com.svg", title: "Home", msg:11 },
        {
          id: 1,
          imageUrl: "/icons/check-mark-button-svgrepo-com.svg",
          title: "Completed", msg:3
        },
        { id: 1, imageUrl: "/icons/calendar-svgrepo-com.svg", title: "Today", msg:4 },
        {
          id: 1,
          imageUrl: "/icons/personal-account-account-svgrepo-com.svg",
          title: "Personal", msg:4
        },
        { id: 1, imageUrl: "/icons/briefcase-svgrepo-com.svg", title: "Work", msg:11 },
      ],
      workspaces: [
        { id: 1, borderColor: "border-violet-500", title: "Otadask" },
        { id: 1, borderColor: "border-blue-500", title: "Nexus" },
        { id: 1, borderColor: "border-green-500", title: "Evrestudio" },
        
      ],
    };
  },
};
</script>
<template>
  <div class="relative h-screen">
    <div class="absolute w-80 h-full  bg-gray-100">
      <div class="mx-6">
        <SideHead />
        <SideBodyPrivate :posts="posts" />
        <SideBodyWorkspace :workspaces="workspaces"/>
      </div>
    </div>
  </div>
</template>

<style>
* {
  font: TwitterChirp, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Helvetica, Arial, sans-serif;
}
svg {
  @apply text-gray-400;
}
</style>
