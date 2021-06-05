<template>
  <div class="home">
    <h1>formularios con vue</h1>
    <div>
      <form @submit.prevent="procesar">
<!--        nombre-->
        <input type="text"
               class="form-control my-2"
               placeholder="escribe tu nombre"
               v-model.trim="tarea.nombre"
        >
        <hr>
<!--        primer checkbox-->
        <div class="form-check form-check-inline">
          <input type="checkbox"
                 id="check-1"
                 class="form-check-input"
                 v-model="tarea.categorias"
                 value="javascript"
          >
          <label for="check-1" class="form-check-label">
            JavaScript
          </label>
        </div>
        <hr>
<!--        segundo checkbox-->
        <div class="form-check form-check-inline">
          <input type="checkbox"
                 id="check-2"
                 class="form-check-input"
                 v-model="tarea.categorias"
                 value="nodejs"
          >
          <label for="check-2" class="form-check-label">
            Node.js
          </label>
        </div>
        <hr>
<!--        radio button urgente-->
        <div class="form-check form-check-inline">
          <input type="radio"
                 id="radio-1"
                 class="form-check-input"
                 value="urgente"
                 v-model="tarea.estado"
          >
          <label for="radio-1"
                 class="form-check-label"
          >
            urgente
          </label>
        </div>
<!--        radio button normal-->
        <div class="form-check form-check-inline">
          <input type="radio"
                 id="radio-2"
                 class="form-check-input"
                 value="normal"
                 v-model="tarea.estado"
          >
          <label for="radio-2"
                 class="form-check-label"
          >
            normal
          </label>
        </div>
<!--        radio button simple-->
        <div class="form-check form-check-inline">
          <input type="radio"
                 id="radio-3"
                 class="form-check-input"
                 value="simple"
                 v-model="tarea.estado"
          >
          <label for="radio-1"
                 class="form-check-label"
          >
            simple
          </label>
        </div>
        <hr>
<!--        numero-->
        <div class="mt-2">
          <input type="number"
                 v-model="tarea.numero"
          >
        </div>
        <hr>
<!--        submit-->
        <button type="submit" class="btn btn-dark">
          procesar
        </button>
      </form>
      <hr>
      <p>
        {{ tarea.nombre }} - {{ tarea.categorias }} - {{ tarea.estado }} - {{ tarea.numero }}
      </p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      tarea: {
        nombre: '',
        categorias: [],
        estado: '',
        numero: 0,
      }
    }
  },
  methods: {
    procesar() {
      console.log(this.tarea)
    }
  }
}
</script>
