<script>
import SideWorkspace from "./SideWorkspace.vue";
import SideWorkspaceCreate from "./SideWorkspaceCreate.vue";
export default {
  components: { SideWorkspace, SideWorkspaceCreate },
  props: {
    workspaces: {
      type: Array,
      required: true,
    },
  },
};
</script>

<template>
  <div class="main-text">
    <p>Workspace</p>
    <div class="ml-2">
      <side-workspace v-for="workspace in workspaces" :workspace="workspace" />
      <SideWorkspaceCreate />
    </div>
  </div>
</template>
