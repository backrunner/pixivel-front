<template>
  <div class="nav nav-hori">
    <div class="nav-circle" @click="routerChange('Rank')">
      <b-icon pack="uil" icon="uil-list-ul"></b-icon>
    </div>
    <div class="nav-circle" @click="routerChange('Search')">
      <b-icon pack="uil" icon="uil-search"></b-icon>
    </div>
    <div class="nav-circle nav-center" @click="routerChange('Landing')">
      <img class="icon" src="../assets/images/favicon.png" />
    </div>
    <div class="nav-circle" @click="routerChange('Account')">
      <b-icon pack="uil" icon="uil-user"></b-icon>
    </div>
    <div class="nav-circle" @click="$router.back()">
      <b-icon pack="uil" icon="uil-angle-left"></b-icon>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nav",
  watch: {},
  data: () => ({}),
  methods: {
    routerChange(name) {
      if (name != this.$route.name) {
        this.$router.push({
          name,
        });
      }
    },
  },
};
</script>

<style lang="scss">
@media screen and (max-width: 790px) {
  .nav-hori {
    padding: {
      top: 0.35rem;
      bottom: 0.35rem;
    }

    position: fixed;
    bottom: 20px;
    margin: 0 auto;
    text-align: center;
    width: 70%;
    max-width: 16rem;
    left: 0;
    right: 0;
    height: 3rem;
    z-index: 100;
    background: rgb(255, 255, 255);
    display: flex;
    align-items: center;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);

    border: {
      radius: 1.5rem;
    }

    .nav-circle {
      width: 2.3rem;
      height: 2.3rem;
      border-radius: 50%;
      flex: 1;
      text-align: center;

      margin: {
        left: 0.5rem;
        right: 0.5rem;

        top: 0.35rem;
        bottom: 0.35rem;
      }
      &:hover {
        background-color: rgb(240, 240, 240);
      }
      &:active {
        background-color: rgb(240, 240, 240);
      }
      display: flex;
      transition: all 0.2s ease-in-out;
      align-content: center;
      justify-content: center;
      align-items: center;
    }

    .nav-center {
      width: 2.3rem;
      height: 2.3rem;
      border-radius: 50%;
      margin: auto;
      background-color: rgb(255, 255, 255);
      flex: 1;
      text-align: center;

      margin: {
        left: 0.5rem;
        right: 0.5rem;

        top: 0.23rem;
        bottom: 0.23rem;
      }
    }
  }
}

@media screen and (min-width: 790px) {
  .nav {
    padding: {
      top: 0.35rem;
      bottom: 0.35rem;
    }

    position: fixed;
    bottom: 20px;
    left: 20px;
    width: 3rem;
    z-index: 100;
    background: rgb(255, 255, 255);
    transition: hover 0.2s ease-in-out;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);

    border: {
      radius: 2rem;
    }

    .nav-circle {
      width: 2rem;
      height: 2rem;
      border-radius: 1rem;

      margin: {
        left: 0.5rem;
        right: 0.5rem;

        top: 0.35rem;
        bottom: 0.35rem;
      }

      display: flex;
      transition: all 0.2s ease-in-out;
      align-content: center;
      justify-content: center;
      align-items: center;

      &:hover {
        background-color: rgb(240, 240, 240);
      }
      &:active {
        background-color: rgb(240, 240, 240);
      }
    }

    .nav-center {
      width: 2.9rem;
      height: 2.9rem;
      border-radius: 1.5rem;
      margin: auto;
      background-color: rgb(255, 255, 255);

      margin: {
        top: 0.23rem;
        bottom: 0.23rem;
      }
    }

    .icon {
      width: 60%;
      height: 60%;
    }
  }
}

@media (prefers-color-scheme: dark) {
  .nav {
    background-color: #1c1c1c;
    .nav-center {
      background-color: #1c1c1c;
    }
    .nav-circle {
      &:hover {
        background-color: #4a4a4a;
      }
      &:active {
        background-color: #4a4a4a;
      }
    }
  }
}
</style>
