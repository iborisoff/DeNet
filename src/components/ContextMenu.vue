<script setup>

</script>

<template>
  <div class="contextmenu-wrapper">
    <ul>
      <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/download.svg"
            alt="upload"
        >
        <span class="menu-item-text">Download</span>
      </li>
      <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/share.svg"
            alt="upload"
        >
        <span class="menu-item-text">Share</span>
      </li>
      <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/trash.svg"
            alt="upload"
        >
        <span class="menu-item-text">Delete</span>
      </li>
      <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/download.svg"
            alt="upload"
        >
        <span class="menu-item-text upload-active">Upload</span>
      </li>
      <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/add_folder.svg"
            alt="upload"
        >
        <span class="menu-item-text">New folder</span>
      </li>
       <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/rename.svg"
            alt="upload"
        >
        <span class="menu-item-text">Rename</span>
      </li>
       <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/copy.svg"
            alt="upload"
        >
        <span class="menu-item-text">Copy</span>
      </li>
       <li class="menu-item">
        <img
            class="base-img"
            src="../assets/icons/info.svg"
            alt="upload"
        >
        <span class="menu-item-text">Info</span>
      </li>
    </ul>
  </div>
</template>

<style lang="scss">
@import "../assets/styles/variables";


.contextmenu-wrapper {
  height: auto;
  width: 150px;
  background-color: white;
  border-radius: 8px;
  box-shadow: 7px 9px 27px 0px rgba(0, 0, 0, 0.12);
  z-index: 100;
}

.new-folder-btn {
  &:hover {
    background-color: black;
    border: 2px solid rgba(172, 173, 181, 1);
  }
}

.menu-item {
  list-style: none;
  width: 100%;
  height: 44px;
  padding: 10px 12px;
  display: flex;
  justify-content: flex-start;
  text-align: left;
  align-items: center;
  line-height: 22.4px;
  border-bottom: 1px solid $baseWightColor;
  cursor: pointer;


  &:last-child {
    border-bottom: none;
  }

  &:hover {
    background-color: $baseWightColor;
  }


  &-text {
    color: $baseGretText;
    font-weight: 300;
    margin-left: 6px;
  }

}

</style>
