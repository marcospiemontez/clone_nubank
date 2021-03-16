<template>
  <q-page class="row q-gutter-sx flex flex-center">
    <div class = "row q-gutter-sx flex flex-center" v-if="$q.platform.is.mobile">
      <div class=" flex flex-center row items-center justify-around container-logo">
      <q-img src="../assets/logo-white.png" width="55px" />
      <strong> Marcos</strong>
      </div>
      <q-icon name="keyboard_arrow_down" size="28px" class="q-icon-arrow"/>
    <q-card class="my-card q-ma-lg" flat bordered>
      <q-card-section horizontal class="q-pa-lg">
        <div class="container-card q-mt-sm">
          <q-icon name="payment" size="30px" class="q-icon-card"/>
          <div class="info-container q-mt-xl">
            <strong class="text-uppercase">Fatura atual</strong>
            <h4 class="q-ma-none">R$ 1.738,87</h4>
            <div>
              <span>Limite disponível</span>
              <strong class="q-ml-sm text-uppercase"> 5.350,00</strong>
            </div>
          </div>
        </div>
        <div>
        <q-card-actions vertical class="column justify-center"/>
        <div class="div-orange" style="border-top-left-radius:5px; border-top-right-radius:5px "></div>
        <div class="div-blue"></div>
        <div class="div-green" style="border-bottom-left-radius:5px; border-bottom-right-radius:5px"></div>
        </div>
      </q-card-section>
      <div class="bottom-container row items-center justify-between q-pa-sm q-mb-md q-mx-sm">
        <q-icon size="25px" name="fastfood"/>
        <span class="q-mx-sm"> Compra mas recente em Pizzaria do Orlando no valor de R$ 45,00 hoje
          <q-icon size="20px" name="keyboard_arrow_right" />
        </span>
      </div>
    </q-card>

    <q-scroll-area horizontal class=" q-my-md">
      <div class="row no-wrap">

        <q-card class="card-items column justify-between q-ml-sm">
          <q-card-section>
            <q-icon name="person_add" size="35px"/>
          </q-card-section>

          <q-card-section class="q-pt-none">
            <strong>Indicar amigos</strong>
          </q-card-section>
        </q-card>
        <q-card class="card-items column justify-between q-ml-sm">
          <q-card-section>
            <q-icon name="monetization_on" size="35px"/>
          </q-card-section>

          <q-card-section class="q-pt-none">
            <strong>Depositar</strong>
          </q-card-section>
        </q-card>
        <q-card class="card-items column justify-between q-ml-sm">
          <q-card-section>
            <q-icon name="request_quote" size="35px"/>
          </q-card-section>

          <q-card-section class="q-pt-none">
            <strong>Transferir</strong>
          </q-card-section>
        </q-card>
        <q-card class="card-items column justify-between q-ml-sm">
          <q-card-section>
            <q-icon name="receipt" size="35px"/>
          </q-card-section>

          <q-card-section class="q-pt-none">
            <strong>Pagar boleto</strong>
          </q-card-section>
        </q-card>
      </div>
    </q-scroll-area>
    </div>
    <div v-if="$q.platform.is.desktop">
      <p class="text-h3 text-white">
        Essa aplicação só é visível via smartphone !!!
        <br/>
        Tente acessar por telefone.
      </p>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
};
</script>

<style lang="scss">

.container-logo {
  width: 40%;
  strong {
    color: $white;
    font-size: 22px;
  }
}

.q-icon-arrow {
  color: $white;
}

.my-card {
  width: 100%;
  max-width: 330px;
  height: 340px;
}

.container-card {
  width: 95%;

}

.q-icon-card {
  color: $gray;
}

.info-container {
  height: 100px;
  h4 {
    color: $blue;
    font-weight: bold;
  }

  strong:first-child {
    color: $blue;
  }

  span {
  color: $gray;
  font-weight: 400;
  }

  strong {
    color: $green;
  }
}

.div-orange {
  height: 30px;
  width: 7px;
  background-color:$orange;
}

.div-blue {
  height: 70px;
  width: 8px;
  background-color: $blue;
}

.div-green {
  height: 105px;
  width: 7px;
  background-color: $green;
}

.bottom-container {
  .q-icon {
    color: $gray;
  }
 span {
  color: gray;
  width: 80%;
  }
}

.card-items {
  height: 140px;
  width: 115px;
  background-color: $purpleDark;
  color: $white;
  cursor: pointer;
}

.q-scrollarea {
  width: 95%;
  height: 145px;
}

</style>