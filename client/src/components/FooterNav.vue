<template>
  <div class="nav">
    <a href="/" class="nav-item" active>
      <HomeIcon :size="20" /> Home
    </a>
    <a href="/discover" class="nav-item">
      <MagnifyIcon :size="20" /> Discover
    </a>
    <a href="/activity" class="nav-item">
      <HeartPulseIcon :size="20" /> Activity
    </a>
    <a href="/profile" class="nav-item">
      <AccountIcon :size="20" /> Profile
    </a>
  </div>
</template>

<script>
import HomeIcon from 'vue-material-design-icons/Home';
import AccountIcon from 'vue-material-design-icons/Account';
import MagnifyIcon from 'vue-material-design-icons/Magnify';
import HeartPulseIcon from 'vue-material-design-icons/HeartPulse';

export default {
  name: 'Nav',
  components: {
    HomeIcon, AccountIcon, MagnifyIcon, HeartPulseIcon
  }
};
</script>

<style lang="scss" scoped>
.nav {
  height: 56px;

  display: flex;
  flex-direction: row;

  background-color: #f1f1f1;

  // border-top-left-radius: 22px;
  // border-top-right-radius: 22px;

  border-top: 1px solid #d3d3d3;

  // box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.75);
}

.nav-item {
  flex: 1;

  position: relative;

  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  text-decoration: none;
  font-family: "Montserrat", sans-serif;
  font-size: 12px;

  color: #1f1f1f;

  .material-design-icon {
    color: #939393;
  }

  &[active] {
    .material-design-icon {
      color: #1f1f1f;
    }
  }
}
</style>