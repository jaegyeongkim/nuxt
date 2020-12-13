<template>
  <v-row justify="center" align="center">
    <v-col  cols="12" sm="8" md="6">
      
      
      <div class="text-center" >
        <v-card class="text-center justify-center">
          <v-card-title class="heacdline">
            신이 {{ $route.params.text_value }}을(를) 만들 때..
          </v-card-title>
          <div class="text-center justify-center margin_bottom">
            <img :src="`${image_path}`">
          </div>   
          <div >
              <router-link :to="{name:'index', params:{text_value:text_value}}">
              <v-btn
                class="margin_bottom"
                color="primary"
                nuxt
              >
                다시하기
              </v-btn>
            </router-link>
          </div> 
        </v-card>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      image_paths: [
        "https://lh5.googleusercontent.com/pSBPdrgWE8CGg9fD5mwSs90-5M-nyHg3MG88mEFCdhp35xStRboh3sBvHw95QAgtkFwfv_XOFKxg0lglLY3-=w1920-h937",
        "https://lh4.googleusercontent.com/_OqyYLkdX7AcnF2tBYFS-3ev-ROFS0PP3CBmEqHsHm9gMm_lpAinif2ydjW53XgapDS-36T_7twjvGgGypEO=w1920-h937",
        "https://lh6.googleusercontent.com/G5YlkNYGXlFPZ6eHlhAzgJjHw6Ie5iUnEl47jsd4siYwdc2pjj2NT3CIDpCe5bkTY-xTV7vE0QKUmt4_u0ru=w1920-h937",
        "https://lh4.googleusercontent.com/tMEHKnds5GkVgmkvEenM9Y0BKBu1v4yUiIRWHmM1QQlv4Uvg992XlGnLfHYpEDQrGVDjU1rzz1VO7LhTXrXX=w1920-h937",
        "https://lh3.googleusercontent.com/vGpG7yta_ZTv1SiIROntlMLwVmU9iRoNF1pMLIAz6pb2Iv8cwwQxQ4EZq1EcMIh_xscOz97yuonI3mUEk9Yo=w1920-h937",
        "https://lh3.googleusercontent.com/MnGNOOjyVXoXB6F67LYZewP9AiwrwYDXA0Nbem3O7kIMIZ-WS_A4SSftCN7hKIVz-CCWy166bEiS10e5CcRM=w1920-h937",
        "https://lh4.googleusercontent.com/mQP17FI9fEL0tqp8AJbOICSQAmqCrj688g_ZBW_l3CRO0b6KZ9p6vtRsNTvl_wGA1viBFuni9F5CC2EBog4-=w1920-h937",
        "https://lh5.googleusercontent.com/wM-aTMBtYu_7PsDcZALO2UuXKLbuO0BovCwOvHbT2FRvxf3MFTZ6b-LIKo2guXRaH1XKqnJqHwj4QFtbENZN=w1920-h937" ,
        "https://lh4.googleusercontent.com/Ql-FBjbFwp4nDsLjdi5zU4lEG2xC1qvT2SwxKk0qQ_6LW1K3F3i5NAMQ7tu7-rDY2aHeAhZNjPlp4GR0JGEa=w1920-h937" ,
        "https://lh5.googleusercontent.com/aEYRGMNOUV0If9rInQchaT6X6OIMD6dJUYTTw_AJrf8cP_iTd0EpIJvxleUjdz_lPm8n5dyRUrFthYRGoBd8=w1920-h937" ,

      ],
      image_path: ''
    }
  },
  created() {
    this.fetchData()
  },
  methods: {
    fetchData() {
      const paths_length = this.image_paths.length-1
      const id = Math.floor((Math.random()*paths_length))
      this.image_path = this.image_paths[id]
    }
  }
};

</script>

<style>
    .margin_bottom {
      margin-bottom:10px;
    }
</style>
