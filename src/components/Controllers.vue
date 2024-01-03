<script>

import SortDrpodown from "@/components/SortDropdown.vue";

export default {
  name: "ControllersElement",
  components: {SortDrpodown}
}

</script>

<template>
  <div class="page-controllers">
    <button class="all-files base-btn">
      All files
    </button>
    <SortDrpodown/>
  </div>
</template>

<style scoped lang="scss">
@import "../assets/styles/variables";

.page-controllers {
  padding: 10px 16px;
  display: flex;
  align-content: center;
  justify-content: space-between;
  margin: 0 auto;
}

.all-files {
  width: 83px;
  height: 32px;
  display: flex;
  justify-content: center;
  margin: auto 0;
  text-align: center;
  padding: 8px 10px;
  color: $baseGretText;
}


</style>
