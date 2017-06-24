<template>
  <div class="container" style="margin-top: 10px;">

    <div class="form-group row">
      <div class="col-6">
        Data:
        <input v-model="date" class="form-control" ref="datepicker">
      </div>
    </div>

    <ul class="nav nav-tabs">
        <li class="nav-item">
          <a v-on:click="cardapio($event)" class="nav-link" href="#">Cardápio</a>
        </li>

        <li class="nav-item">
          <a v-on:click="comments($event)" class="nav-link active" href="#">Comentários</a>
        </li>
    </ul>

    <h3>EMEF ALVARES DE AZEVEDO</h3>
    <p>
      2 A 6 ANOS ...
    </p>

    <h5>Comentários da Comunidade</h5>
    <hr>
    <p></p>

    <div style="font-size: 19px;">
      <button style="background-color: #005653" class="mdl-button mdl-js-button mdl-button--fab mdl-button--colored">
        <i class="material-icons">chevron_left</i>
      </button>
      <br>
      Voltar
    </div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        date: "24/03/2017"
      }
    },
    created() {

    },
    mounted() {

      jQuery(this.$refs.datepicker).datepicker();
      var d = new Date();
      this.date = d.getDay() + "/" + d.getMonth() +  "/" + d.getFullYear();
      jQuery(this.$refs.datepicker).val(this.date);

    },
    methods: {

        comments(event) {
            event.preventDefault();
            this.$router.push({ path: '/school/comments' })
        },

        cardapio(event) {
            event.preventDefault();
            this.$router.push({ path: '/school' })
        }

    }
  }
</script>

<style scoped>
  h3, strong {
    color: #bc2026 !important;
  }
</style>
