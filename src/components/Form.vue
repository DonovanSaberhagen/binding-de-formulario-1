<template>
    <div id="app">
      <form>
        <div>
          <label>Título de la tarjeta: </label>
          <input v-model="title"/>
        </div>
        <div>
          <label>Chip SRC: </label>
          <input v-model="chip"/>
        </div>
        <div>
          <label>Número: </label>
          <input v-model="number"/>
        </div>
        <div>
          <label>Fecha de expiración: </label>
          <input v-model="date"/>
        </div>
        <div>
          <label>Propietario: </label>
          <input v-model="owner" />
        </div>
        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input v-model="cardType"/>
        </div>
      </form>
  
      <div class="carnet">
        <h3>{{ title }}</h3>
        <img width="40" :src="chip" alt="Chip" />
        <div>
          <h2>{{ number }}</h2>
          <span> Fecha de Exp: {{ date }}</span>
        </div>
        <footer>
          <span>{{ owner }}</span>
          <img :src="cardType" width="60" alt="Visa"/>
        </footer>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'BindingForms',
    data() {
      return {
        title: '',
        chip: '',
        number: '',
        date: '',
        owner: '',
        cardType: '',
  
      }
    },
    props: {
      msg: String
    }
  }
  </script>
  
  <!-- Css -->
  <style scoped>
  * {
    margin: 0;
  }
  
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 60vh;
    font-size: 10px;
    font-family: sans-serif;
  }
  
  #app {
    display: flex;
    gap: 40px;
  }
  
  form {
    padding: 18px;
    border-radius: 20px;
    border: ridge 1px;
    box-shadow: 1px 1px 1px 1px gray;
    font-weight: bold;
    display: flex;
    flex-direction: column;
    gap: 15px;
    justify-content: center;
  }
  
  form div {
    display: grid;
    grid-template-columns: 100px 200px;
    align-items: center;
    gap: 5px;
  }
  
  form div label {
    text-align: right;
  }
  
  .carnet {
    width: 400px;
    height: 230px;
    background: #1c1a1e;
    color: white;
    border-radius: 20px;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  h3 {
    font-size: 20px;
  }
  
  h2 {
    font-size: 30px;
    letter-spacing: 10px;
    margin-bottom: 15px;
    text-shadow: 0px 0px 1px gold;
    font-family: Times;
  }
  
  b {
    font-size: 16px;
  }
  
  footer {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    font-weight: bold;
    font-size: 18px;
    text-transform: uppercase;
    font-style: italic;
  }
  </style>