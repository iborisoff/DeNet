<script>
import FileListItem from "@/components/FileListItem.vue";

export default {
  name: "FileList",
  components: {
    FileListItem,
  },
}

</script>

<template>
  <div class="list-wrapper">
    <FileListItem/>
    <FileListItem/>
    <FileListItem/>
  </div>
</template>

<style scoped lang="scss">
.list-wrapper {
  margin-top: 15px;
  display: flex;
}


.folder-img {
  height: 90px;
  width: 120px;
}

</style>
