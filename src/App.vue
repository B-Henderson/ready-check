<template>
  <div id="app">
    <h1>Ready Check</h1>
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/apply">Apply</router-link>
      <transition name="fade" mode="out-in">
        <router-view/>
      </transition>
    </div>
  </div>
</template>

<style lang="scss">
.info-container,
.apply-container {
  width: 800px;
  background-color: #444;
  border: 1px solid #555;
  margin-top: 30px;
  box-shadow: 0px 2px 10px 0px rgba(0, 0, 0, 0.16),
    0px 2px 5px 0px rgba(0, 0, 0, 0.26);
  padding: 2rem 1rem;
  .info-sec,
  .apply-sec {
    width: 100%;
    margin: 1rem 1rem;
    display: flex;
    align-content: space-between;
    justify-content: space-between;
    line-height: 1.8rem;
    flex: 0 100%;
    .rowdata {
      margin-right: 0.25rem;
    }

    .classnames:last-child {
      margin-right: 0;
    }
    .data-key {
      text-decoration: underline;
    }
    * {
      font-size: 1.2rem;
      //   flex: 0 50%;
    }
  }
}
.app {
  display: flex;
  align-content: center;
  justify-content: center;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
h1 {
  font-size: 4rem;
  line-height: 2rem;
  font-family: "Orbitron", "Avenir", Helvetica, Arial, sans-serif;
  font-weight: 700;
  color: rgba(200, 163, 15, 1);
}
.druid {
  color: rgba(255, 125, 10, 0.8);
}
.hunter {
  color: rgba(169, 210, 113, 0.8);
}
.mage {
  color: rgba(64, 199, 235, 0.8);
}
.priest {
  color: rgba(255, 255, 255, 0.8);
}
.rogue {
  color: rgba(255, 245, 105, 0.8);
}
.shaman {
  color: rgba(0, 112, 222, 0.8);
}
.warlock {
  color: rgba(135, 135, 237, 0.8);
}
.warrior {
  color: rgba(199, 156, 110, 0.8);
}
span.spacer {
  color: #ff3333;
}

body {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #eee;
  background-color: #333;
  font-family: "Roboto", "Calibri", sans-serif;
  letter-spacing: 1px;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #eee;

    &.router-link-exact-active {
      color: rgba(200, 163, 15, 1);
    }
  }
}
</style>
