<template>
  <div class="profile">
    <div class="p-nav">
      <div class="p-nav__left">
        <ChevronLeft />
      </div>
      <div class="p-nav__content">
        <div class="text text--user">Example User</div>
      </div>
      <div class="p-nav__right">
        <CogIcon />
      </div>
    </div>
    <div class="profile__header">
      <div class="profile-avatar"></div>
      <Button>
        Follow
      </Button>
    </div>
    <div class="profile__content">
      <div class="text text--title">
        Recent Activity
      </div>
    </div>
  </div>
</template>

<script>
import CogIcon from 'vue-material-design-icons/Cog';
import ChevronLeft from 'vue-material-design-icons/ChevronLeft';

export default {
  name: 'Profile',
  components: {
    CogIcon, ChevronLeft
  },
};
</script>

<style lang="scss" scoped>
.profile {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.p-nav {
  padding: 12px;

  display: flex;
  align-items: center;
  justify-content: center;

  flex-direction: row;

  background-color: #f1f1f1;
  border-bottom: 1px solid #d3d3d3;
}

.p-nav__left,
.p-nav__right,
.p-nav__content {
  display: flex;
  align-items: center;
}

.p-nav__left {
  flex: 1;
}

.p-nav__right {
  flex: 1;
  justify-content: flex-end;
}

.material-design-icon {
  display: flex;
  align-items: center;
}

.profile__header {
  padding: 20px;
  border-bottom: 1px solid #d3d3d3;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  & > *:not(:first-child) {
    margin-top: 12px;
  }
}

.text {
  font-family: "Montserrat", sans-serif;
}

.text--title {
  font-size: 18px;
  font-weight: 600;
}

.text--user {
  font-size: 14px;
  font-weight: bold;
}

.text--description {
  font-size: 14px;
}

.profile__content {
  flex: 1;
  padding: 20px;
  border-top-left-radius: 22px;
  border-top-right-radius: 22px;
  top: -20px;
}

.profile-avatar {
  width: 96px;
  height: 96px;
  border-radius: 100%;
  background-color: blue;
}
</style>
