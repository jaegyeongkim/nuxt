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
        "https://lh4.googleusercontent.com/tcgZrptaIUXfi_6Pqpuql8o-exdWYbinzsI6HHqQcOr6T9eGXLd-UPpJI9UtLuCIwDv_p4CuWAIzuwiUgpnT=w1365-h937",
        "https://lh6.googleusercontent.com/qqUg07RNu6wIzvWVt2CSBWs5Tm-f-EZoG1FZR6iGL0yqDSYR41KFmbSFtAOEjn6HmNfmyMksFTl7-9FHA3yr=w1920-h937",
        "https://lh3.googleusercontent.com/f50dODhDFAyLUfoXao5yt-cujmN7oNljA7QQgyr-pvjPswS8_zoBUGLrH5Qh7lJ5ZsluYU8Gkmiksrr2xgbU=w1365-h937" ,
        "https://lh5.googleusercontent.com/Ya0vojt8HA6WYbwVeNREwKKiTvVx8GPm-xSBC49B7EuO6RD8BKH0mMtpLCXEh_8sgY0a3cr422CJ8ac5XObP=w1365-h937" ,
        "https://lh4.googleusercontent.com/KE1sBdIC4Ipd4lEoexM25--vlU2F_hRmxg2xy-PtatNO5pbOMLLd72XONY84KvjgPuOyJG2LX3ruI3q8ow__=w1365-h937" ,
        "https://lh4.googleusercontent.com/1plYnLmnu6Z6HdVEKSB0oxISucDevkkZQNvRXw45eNKQvtHSoHjq8Njx0CX_KOxoXmVFIYQ_pyb1ojQi5LmD=w1365-h937" ,
        "https://lh4.googleusercontent.com/B1oLGIiCnNemtnvDrtccYkO6nYazRXE4hsRuES4uFPfb5S9mdh5Y0dwoowviwF6q29TM6rQO9Mcyuc_6FhLr=w1365-h937" ,
        "https://lh3.googleusercontent.com/j8E8Ik_TK0T__OYg0uB3SZBsI6wZyIZe_PGQJS7jBOEGizteyh3Uco9aFE4My3N2nknL8aVcN8RYNOuE07R7=w1365-h937" ,
        "https://lh4.googleusercontent.com/9HlWHPF67K1YXRMe23JG0tXwE9O4sGKHH6oF3qLX9UMwhIDaD9PZw7qvxVBoXBCRLGjuH_YT0tfdb80BRzOF=w1365-h937" ,
        "https://lh3.googleusercontent.com/9bZu8OgbvgJStEL3AHobE37Lv5GCS3Sw65fgq4pYpcWFkXZh9uJOu7G7epdpM7exv1gMnhjEYGrI4yAS8IHC=w1365-h937" ,
        "https://lh3.googleusercontent.com/hJs_IlBzZKyXaxvVMU6zvHh4gXYlkbtp-hbQgSOZUwFvvQ5c53fY2QJM7asUmMhf08XkR4IGk5f6zCXQPpzD=w1365-h937" ,
        "https://lh3.googleusercontent.com/eRzY6PMS1CE4LxlZ0WQ0cFgX4RievlW6Dae23Vb52nOWc84QKEiokPDN7QOVgSWeZDovgAfFPmRxcUlWuRsv=w1365-h937" ,
        "https://lh5.googleusercontent.com/23EhE3OLXke9ktUpEMl0Hv4ztl-Soj4N45vdpPexhTSX1cixldylGPvubGJqQgpErk420kq3rtF8OWTdNsqf=w1365-h937" ,
        "https://lh5.googleusercontent.com/4Y-T6MjTWeA2n-NzcuWvioxGyef62NSCsxjaZ9nTGgfSQcK3Osa24E5vTDHuVxxGGF1mALfbSSoGz3r6EHVV=w1365-h937" ,
        "https://lh3.googleusercontent.com/T1CgEzCM4rnuyF9e5V_rDNRGVsIVos7AITP82E1GHrbjMPIEyIqdjr_vyw9BewSAPeab6FG7lwSbF21o3RCE=w1365-h937" ,
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
