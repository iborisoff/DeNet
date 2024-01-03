<template>
  <div class="page-wrapper">
    <Header />
    <div class="content-wrapper">
      <Controllers />
      <FileList />
    </div>
    <button class="delete-btn base-btn">
      <img
          alt="trash"
          class="base-img"
          src="../assets/icons/trash.svg"
      />
      Recycle bin
    </button>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Controllers from "@/components/Controllers.vue";
import FileList from "@/components/FileList.vue";
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    Header,
    Controllers,
    FileList,
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/variables.scss';

.page-wrapper{
  position: relative;
}

.delete-btn {
  position: absolute;
  right: 30px;
  bottom: 20px;
  width: 144px;
  height: 40px;
  padding: 8px 7px 8px 7px;
  border-radius: 14px;
  box-shadow: 0px 3px 19px 0px rgba(35, 35, 35, 0.12);

  &:hover {
    background-color: transparent;
  }

  img {
    margin-right: 6px;
  }
}

.content-wrapper {
  position: relative;
  width: 100%;
  height: auto;
  padding: 0 50px;
}
</style>
