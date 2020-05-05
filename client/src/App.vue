<template>
  <div id="app">
    <div class="app-wrapper">
      <div class="app__content">
        <keep-alive>
          <router-view/>
        </keep-alive>
      </div>
      <div class="app__footer">
        <FooterNav />
      </div>
    </div>
  </div>
</template>

<script>
import FooterNav from '@/components/FooterNav';

export default {
  name: 'App',
  components: { 
    FooterNav,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

input,
textarea,
button,
select,
a {
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}

html,
body,
#app {
  height: 100%;
}

#app {
  display: flex;
  align-items: center;
  justify-content: center;

  background-color: #333333;
}

.app-wrapper {
  position: relative;
  width: 100%;
  height: 100%;

  display: flex;
  flex-direction: column;

  background-color: #f1f1f1;
}

.app__content {
  overflow: auto;

  flex: 1;
  min-height: 0;

  &::-webkit-scrollbar {
    display: none;
  }
}

.app__footer {
  position: absolute;
  bottom: 0;
  width: 100%;
}

@media only screen and (min-width: 960px) {
  // Emulates a mobile aspect ratio when viewed on desktop.
  .app-wrapper {
    position: relative;

    height: 80vh;
    width: calc(80vh / 1.75);

    box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.75);
  }
}
</style>
