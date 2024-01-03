<script>
export default {
  name: "HeaderComponent",
}
</script>

<template>
  <header class="wrapper">
    <img
        class="logo"
        src="../assets/icons/logo.svg"
        alt="logo"
    />
    <button class="upload-btn base-shadow-btn">
      <img
          src="../assets/icons/upload.svg"
          alt="upload file"
          class="base-img"
      />
      <span>Upload</span>
    </button>
    <button class="add-folder-btn base-shadow-btn">
      <img
          src="../assets/icons/add_plus.svg"
          alt="add folder"
          class="base-img"
      />
      <span>New Folder</span>
    </button>
    <button class="recycle-bin-btn base-btn">
      <img
          alt="trash"
          src="../assets/icons/trash.svg"
          class="base-img"
      />
      <span>Recycle bin</span>
    </button>

    <button class="search-btn base-btn">
      <img
          class="base-img"
          src="../assets/icons/search.svg"
          alt="search"
      />
    </button>
    <div class="network-dropdown base-outline-container">
      <img
          src="../assets/icons/link.svg"
          alt="link"
      />
      <span>Polygon</span>
      <button class="base-btn">
        <img
            class="base-img"
            alt="drop down arrow"
            src="../assets/icons/arrow-down.svg"
        />
      </button>
    </div>
    <div class="balance base-outline-container">
      <span class="usage-text">Used:</span>
      <span class="usage-value">0.4 GB</span>
      <div class="vertical-line"/>
      <span class="balance-text">Balance:</span>
      <span class="balance-value">0.6 TBY</span>
      <button class="base-btn">
        <img
            src="../assets/icons/plus-yellow.svg"
            alt="Add balance"
            class="yellow-plus base-img"
        >
      </button>
    </div>
    <button class="avatar base-btn">
      <img
          alt="profile"
          src="../assets/icons/profile.svg"
      />
    </button>
  </header>
</template>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";


.wrapper {
  padding: 32px 64px;
  height: 104px;
  width: 100%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.logo {
  width: 200px;
  height: 24px;
}

.add-folder-btn, upload-btn, recycle-bin-btn {
  img {
    margin-right: 10px;
  }
}


.add-folder-btn {
  padding: 10px 14px;
  width: 160px;
  min-width: auto;
  border: 2px solid transparent;

  &:hover {
    border: 2px solid rgba(35, 35, 35, 0.08);
  }

}

.yellow-plus {
  height: 18px;
  width: 18px;
  margin-left: 12px;
}

.upload-btn {
  padding: 10px 20px;
  width: 138px;
  margin-right: 20px;
  margin-left: 28px;

  &:hover {
    background-color: $baseYellow;
  }

}

.recycle-bin-btn {
  width: 164px;
  padding: 10px 14px;
  margin-left: 20px;
}

.add-folder-btn, .upload-btn, .recycle-bin-btn {
  img {
    margin-right: 10px;
  }
}

.search-btn {
  height: 40px;
  width: 40px;
  border-radius: 100%;
  background-color: $baseGreyColor;
  margin-left: auto;
  margin-right: 18px;
  padding: 0;

  img {
    margin: auto;
  }
}

.network-dropdown {
  display: flex;
  align-items: center;
  align-content: center;
  padding: 8px 16px;
  cursor: pointer;
  margin-right: 10px;

  span {
    margin-right: 43px;
    margin-left: 6px;
    line-height: 19.5px;
  }
}

.balance {
  padding: 10px 16px;

  .vertical-line {
    height: 100%;
    width: 4px;
    background-color: $baseWightColor;
    margin: 0 12px;
  }

  .usage {
    &-value, &-text {;
      width: max-content;
    }
     &-value {
      margin-left: 2px;
    }
  }
  .balance {
    &-text, &-value {
      width: max-content;
    }
    &-value {
      margin-left: 2px;
    }
  }

  .usage-text, .balance-text {
    color: $baseGretText;
    font-weight: 300;
  }
}


.avatar {
  margin-left: 22px;
}

</style>
