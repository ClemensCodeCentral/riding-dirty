<template>
  <div id="app">
    <header>
      <span>Riding Dirty?</span>
    </header>
    <main>
      <div class="container">
        <div class="title" v-for="crime in crimes" :key="crime" >
          <div>{{ crime.name }}</div>
          <div>{{ crime.points }}</div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      crimes: [
        {
          name: "Weed",
          points: 1
        },
        {
          name: "Meth",
          points: 5
        },
        {
          name: "Suspended license",
          points: 10
        },
        {
          name: "Other illegal drugs",
          points: 15
        },
        {
          name: "????",
          points: 15
        },
        {
          name: "Hostage",
          points: 100
        },
      ]
    }
  }
}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

main {
  text-align: center;
  margin-top: 40px;
}

header {
  margin: 0;
  height: 56px;
  padding: 0 16px 0 24px;
  background-color: #35495E;
  color: #ffffff;
}

header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: .02em;
  font-weight: 400;
  box-sizing: border-box;
  padding-top: 16px;
}

@media (max-width: 720px) {
  .title {
    width: 100%;
  }

  .container {
    padding: 16px;
    display: grid;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 721px) {
  .title {
    width: 100%;
  }

  .container {
    padding: 16px;
    display: grid;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
    grid-template-columns: repeat(16, 1fr);
  }

}

.title {
  background: gray;
  padding: 4px;
}

.container {
  padding: 16px;
  display: grid;
}
</style>
