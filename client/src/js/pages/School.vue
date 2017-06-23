<template>
  <div class="container" style="margin-top: 10px;">

    <div class="form-group row">
      <div class="col-6">
        Data:
        <input v-model="data" class="form-control" ref="datepicker">
      </div>
    </div>

    <ul class="nav nav-tabs">
      <li class="nav-item">
        <a class="nav-link active" href="#">Cardápio</a>
      </li>

      <li class="nav-item">
        <a class="nav-link" href="#">Comentários</a>
      </li>

    </ul>

    <h3>EMEF ALVARES DE AZEVEDO</h3>
    <p>
      2 A 6 ANOS ...
    </p>

    <p>
      <strong>DESJEJUM</strong>
      <p>
        Planejado: Composto Lácteo Cappuccino, Bolo sabor Fubá e Maçã.<br>
        Servido: Composto Lácteo Cappuccino, Bolo Individual sabor Fubá e Maçã.
      </p>

      <strong>ALMOÇO</strong>
      <p>
        Planejado: Arroz, Feijão Carioca, Escondidinho de PTS e Mamão.<br>
        Servido: Arroz, Feijão Carioca, Escondidinho de PTS e Mamão.
      </p>

      <strong>LANCHE</strong>
      <p>
        Planejado: Leite Integral com Achocolatado, Biscoito Salgado e Banana Prata.<br>
        Servido: Leite Integral com Achocolatado, Biscoito Salgado e Banana Prata.
      </p>

    </p>



    <div style="font-size: 19px;">
      <button style="background-color: #6666ff" class="mdl-button mdl-js-button mdl-button--fab mdl-button--colored">
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
        data: "06/30/2017"
      }
    },
    created() {

    },
    mounted() {

      var d = new Date();
      this.date = d.getDay() + "/" + d.getMonth() +  "/" + d.getFullYear();

      jQuery(this.$refs.datepicker).datepicker();

    },
    methods: {
      
      search() {
          alert("Oi")
      }

    }
  }
</script>

<style scoped>
  h3, strong {
    color: #bc2026 !important;
  }
</style>
