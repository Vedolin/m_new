<template>
  <div class="">
      <div class="jumbotron jumbotron-fluid">
          <div class="container">
              <h4 class="text-center">Informações sobre alimentação escolar.</h4>
              <p class="text-center lead">This is a modified jumbotron that occupies the entire horizontal space of its parent.</p>
              <form class="box-form form-inline">
                  <input class="box-search form-control" type="text" placeholder="Digite o nome da escola">
                  <button v-on:click="search()" class="btn btn-outline-success" type="submit">Buscar</button>
              </form>
          </div>
      </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {

      }
    },
    methods: {
      search() {
          alert("Oi")
      }
    }
  }
</script>

<style scoped>
    .box-title {
        width: 45%;
        color: #424242;
        font-family: 'Sofia W01 Bold1446843','Open Sans',sans-serif;
        font-size: 35px;
        margin: 0 auto;
    }

    .box-paragrath {
        width: 55%;
        margin: 0 auto;
    }

    .box-form {
        width: 56%;
        margin: 0 auto;
    }

    .box-search {
        width: 85%;
        margin: 0 auto;
    }

    @media (max-width: 575px) {
        .box-paragrath {
            width: 100%;
            margin: 0 auto;
        }

        .box-form {
            width: 100%;
            margin: 0 auto;
        }

        .box-search {
            width: 70%;
            margin: 0 auto;
        }
    }

    @media (max-width: 767px) {
        .box-paragrath {
            width: 100%;
            margin: 0 auto;
        }

        .box-form {
            width: 100%;
            margin: 0 auto;
        }

        .box-search {
            width: 70%;
            margin: 0 auto;
        }
    }

</style>
