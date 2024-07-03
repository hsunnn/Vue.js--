<script>
import FormComponent from "./components/FormComponent.vue";

export default {
  name: "App",
  components: {
    FormComponent,
  },
};
</script>

<template>
  <header>
    <img class="logo" src="./images/前進.jpg" width="300" height="200" />
  </header>

  <main id="mainposition">
    <TheWelcome />
    <div id="app">
      <FormComponent />
    </div>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
  .mainposition {
    position: center;
  }
}
</style>
