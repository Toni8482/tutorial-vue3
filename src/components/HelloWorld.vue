<template>
  <div>
    <label for="name">Introdueix el teu nom:</label>
    <input id="name" v-model="userName" />

    <p v-if="userName">Benvingut, {{ userName }}!</p>
    <p v-else>Si us plau, introdueix el teu nom.</p>
  </div>
</template>

<script>
export default {
  name: 'WelcomeUser',

  // Dades del component
  data() {
    return {
      userName: '',
    };
  },

  // Mètodes del component
  methods: {
    // Funció per reinicialitzar el nom
    resetName() {
      this.userName = '';
    },
  },
};
</script>

<style scoped>
/* Estils específics per al component */
div {
  margin: 20px;
}

label {
  font-weight: bold;
}

input {
  margin-bottom: 10px;
  padding: 5px;
}

p {
  margin-top: 10px;
}
</style>