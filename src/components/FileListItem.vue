<template>
  <div
      class="file"
      :class="{'active': showContextManu }"
      @contextmenu.prevent="onContextMenuHandler"
      @contextlost.prevent="onContextMenuHandler"
  >
    <img
        class="file-folder-icon"
        src="../assets/icons/folder.svg"
        alt="folder"
    />
    <span>open</span>
    <ContextMenu
        ref="contextMenu"
        v-show="showContextManu"
        class="context-menu-position"
    />
  </div>
</template>
<script>
import ContextMenu from "@/components/ContextMenu.vue"
import { onClickOutside } from '@vueuse/core'

export default {
  name: 'FileListItem',
  data(){
    return {
      showContextManu: false,
    }
  },
  components: {ContextMenu},
  methods: {
    onContextMenuHandler(value){
      this.showContextManu = value;
    },
  },
  mounted() {
    onClickOutside(this.$refs.contextMenu, event => {
      if (event.target.classList === 'file') {
        this.showContextManu = true;
        return;
      }
      this.showContextManu = false;
    })
  }
}
</script>
<style scoped lang="scss">
@import "../assets/styles/variables";

.active {
  border-radius: 8px;
  background-color: $baseWightColor;
}


.file {
  position: relative;
  padding: 25px 15px;
  margin-right: 17px;
  height: 176px;
  width: 150px;

  &-name {
    margin-top: 15px;
  }

  &-folder-icon {
    height: 90px;
    width: 120px;
  }

}

.file:hover {
  border-radius: 8px;
  background-color: rgba(246, 246, 246, 1);
  cursor: pointer;
}

.context-menu-position {
  position: absolute;
  top: 45px;
  left: 150px;
}

</style>
