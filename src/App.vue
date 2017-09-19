<template>
  <div id="app">

  </div>
</template>

<script>
import FireBase from 'firebase'

let config = {
  apiKey: "AIzaSyC2abaJk8IJQwhUIO2zgo_wkK8gDCAIS-4",
  authDomain: "vuejs-books-8c952.firebaseapp.com",
  databaseURL: "https://vuejs-books-8c952.firebaseio.com",
  projectId: "vuejs-books-8c952",
  storageBucket: "vuejs-books-8c952.appspot.com",
  messagingSenderId: "949868469908"
}

let app = FireBase.initializeApp(config)
let db = app.database()

let bookRef = db.ref('books')

export default {
  name: 'app',
  firabase: {
    books: bookRef
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
