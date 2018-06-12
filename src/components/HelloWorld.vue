<template>
  <div class="hello">
    <section>
    <nav>
      <div class="container">
        <input type="text" class="input" placeholder="Buscar canciones..." v-model="searchQuery">
        <button class="btn btn-primary btn-sm" @click="search()">Buscar</button>
        <button class="btn btn-danger btn-sm"> x </button>
      </div>
    </nav>
    <div class="container">
      <ul class="list-group">
        <li class="list-group-item" v-for="t in tracks" :key="t">{{t.name}} - {{t.artist}}</li>
      </ul>
    </div>
      <p>{{searchMessage}}</p>
    </section>
    <!--<h1>{{person.name}}</h1>-->
    <!--<p>{{(a*b).toFixed(2)}}</p>-->
    <!--&lt;!&ndash;convertir a un estring&ndash;&gt;-->
    <!--<p>{{JSON.stringify(person)}}</p>-->
    <!--&lt;!&ndash;se puede usar epresiones ternarias&ndash;&gt;-->
    <!--<p>{{true ? true : false}}</p>-->
    <!--&lt;!&ndash;Mostrar o ocultar el contenido segun el valor&ndash;&gt;-->
    <!--<p v-show="showvalue">Hola</p>-->
    <!--&lt;!&ndash;EL if lo elimina del DOM, mientras que el show solo lo pose en display: none&ndash;&gt;-->
    <!--<p v-if="showvalue">Hola - IF</p>-->
    <!--&lt;!&ndash;se tiene que ubicar debajo del elemento v-if&ndash;&gt;-->
    <!--<p v-else-if="true">Holis</p>-->
    <!--&lt;!&ndash;si no cumple&ndash;&gt;-->
    <!--<p v-else>False</p>-->
    <!--<p>Holis</p>-->
    <!--<ul>-->
      <!--<li v-for="st in items" :key="st">{{st}}</li>-->
    <!--</ul>-->

    <!--<input type="text" v-model="name">-->
    <!--<p>name: {{name}}</p>-->
    <!--<input type="text" v-model="lastName">-->
    <!--<a v-bind:href="url" target="_blank">bind</a>-->

    <!--{{fullName}}-->

    <!--<input type="number" placeholder="Fecha nacimiento" v-model="fechaNacimiento" maxlength="4">-->
    <!--<p>{{fechaNacimiento}} </p>-->
    <!--<p>{{age}} años</p>-->

    <!--<button v-on:click="format()">Format</button>-->
    <!--<p>{{formatName}}</p>-->
  </div>
</template>

<script>
const tracks = [
  {name: 'Muchacha', artist: 'Luis Alberto'},
  {name: 'Hoy aca en el baile', artist: 'El Pepo'},
  {name: 'I was made for loving you', artist: 'kiss'}
]
export default {
  name: 'HelloWorld',
  data () {
    return {
      searchQuery: '',
      tracks: []
    }
  },
  computed: {
    searchMessage () {
      return `Encontrados: ${this.tracks.length}`
    }
  },
  methods: {
    search () {
      // console.log(this.searchQuery)
      this.tracks = tracks
    }
  }

  // data () {
  //   return {
  //     msg: 'Como estas',
  //     showvalue: false,
  //     a: 14.456,
  //     b: 34535.45,
  //     person: {
  //       name: 'Juan'
  //     },
  //     items: ['h', 2, 3],
  //     name: 'Holiss',
  //     url: 'https://www.google.com.pe',
  //     lastName: 'Duran',
  //     fechaNacimiento: '',
  //     formatName: ''
  //   }
  // },
  // // Computed properties son funciones que devuelven un valor y dentro de esta funcion se puede usar propiedades ya existentes
  // computed: {
  //   fullName () {
  //     return `${this.name} ${this.lastName}`
  //   },
  //   age () {
  //     return (new Date().getFullYear()) - this.fechaNacimiento
  //   }
  // },
  // watch: {
  //   fechaNacimiento (newfechaNacimiento, oldfechaNacimiento) {
  //     console.log(newfechaNacimiento, oldfechaNacimiento)
  //   }
  // },
  // methods: {
  //   format () {
  //     this.formatName = this.name.split(' ').join('-').toUpperCase()
  //   }
  //
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
