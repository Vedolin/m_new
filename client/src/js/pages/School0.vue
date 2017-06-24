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

<ul class="demo-list-three mdl-list">
  <li class="mdl-list__item mdl-list__item--three-line">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons mdl-list__item-avatar">person</i>
      <span>Bryan Cranston</span>
      <span class="mdl-list__item-text-body">
        Bryan Cranston played the role of Walter in Breaking Bad. He is also known
        for playing Hal in Malcom in the Middle.
      </span>
    </span>
  </li>
  <li class="mdl-list__item mdl-list__item--three-line">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons  mdl-list__item-avatar">person</i>
      <span>Aaron Paul</span>
      <span class="mdl-list__item-text-body">
        Aaron Paul played the role of Jesse in Breaking Bad. He also featured in
        the "Need For Speed" Movie.
      </span>
    </span>
  </li>
  <li class="mdl-list__item mdl-list__item--three-line">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons  mdl-list__item-avatar">person</i>
      <span>Bob Odenkirk</span>
      <span class="mdl-list__item-text-body">
        Bob Odinkrik played the role of Saul in Breaking Bad. Due to public fondness for the
        character, Bob stars in his own show now, called "Better Call Saul".
      </span>
    </span>
  </li>
  <li class="mdl-list__item mdl-list__item--three-line">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons  mdl-list__item-avatar">person</i>
      <span>Bob Odenkirk</span>
      <span class="mdl-list__item-text-body">
        Bob Odinkrik played the role of Saul in Breaking Bad. Due to public fondness for the
        character, Bob stars in his own show now, called "Better Call Saul".
      </span>
    </span>
  </li>
</ul>




    <div style="font-size: 19px;">
      <button v-on:click="back" style="background-color: #005653" class="mdl-button mdl-js-button mdl-button--fab mdl-button--colored">
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
        },
        back() {
            window.history.back();
        }

    }
  }
</script>

<style scoped>
  h3, strong {
    color: #bc2026 !important;
  }

  .demo-list-three {
    width: 650px;
  }
</style>
