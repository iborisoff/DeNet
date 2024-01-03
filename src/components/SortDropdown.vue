<template>
  <div class="filter-wrapper">
    <div
        @click="onClickHandler"
        class="filter-controllers base-outline-container"
        :class="{'filter-controllers-active': showOptionsList }"
    >
      <span>Sort by name</span>
      <img
          class="base-img"
          alt="dropdown arrow"
          src="../assets/icons/arrow-down.svg"
      >
    </div>
    <div class="dropdown-wrapper" ref="dropdownWrapper" v-show="showOptionsList">
      <button class="dropdown-wrapper-item base-btn"> By type </button>
      <button class="dropdown-wrapper-item base-btn"> By size </button>
      <button class="dropdown-wrapper-item base-btn"> By time </button>
    </div>
  </div>
</template>
<script>
import { onClickOutside } from "@vueuse/core";

export default {
  name: 'SortDropdown',
  data(){
    return {
      showOptionsList: false
    }
  },
  methods: {
    onClickHandler(){
      this.showOptionsList = !this.showOptionsList
    }
  },
  mounted() {
    onClickOutside(this.$refs.dropdownWrapper, (event) => {
        if (event.target.classList !== 'dropdown-wrapper') this.showOptionsList = false
    })
  }
}
</script>
<style scoped lang="scss">
@import "../assets/styles/variables.scss";

.filter-wrapper {
  position: relative;
  margin-left: auto;
  width: 175px;
}

.dropdown-wrapper {
  position: absolute;
  top: 62px;
  box-shadow: 6px 12px 36px 0px rgba(35, 35, 35, 0.1);
  border-radius: 8px;
  width: 175px;
  height: 134px;
  padding: 19px 16px;

  &-item {
    width: 100%;
    height: 20px;
    color: $baseGretText;
    margin: 18px 0;
  }

  &-item:hover {
    background-color: transparent;
  }

  &-item:first-child, &-item:last-child {
    margin: 0;
  }

}


.filter-controllers {
  width: max-content;
  padding: 10px 16px;
  cursor: pointer;

  &-active {
    background-color: transparent;
    border: 1px solid rgba(172, 173, 181, 1);
  }


  &:hover {
    border-radius: 8px;
    border-color: transparent;
    background-color: $baseGreyColor;
  }

  img {
    margin-left: 9px;
  }

}


</style>
