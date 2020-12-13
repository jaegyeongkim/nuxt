<template>
  <v-row justify="center" align="center">
    <v-col  cols="12" sm="8" md="6">
      <div class="text-center" >
        <v-card class="text-center justify-center">
          <v-card-title class="heacdline">
            신이 {{ $route.params.text_value }}을(를) 만들 때..
          </v-card-title>
          <div class="text-center justify-center margin_bottom">
            <img v-if="id == 0" src="~/assets/images/2.png" class="image_size">
            <img v-if="id == 1" src="~/assets/images/3.png" class="image_size">
            <img v-if="id == 2" src="~/assets/images/4.png" class="image_size">
            <img v-if="id == 3" src="~/assets/images/6.png" class="image_size">
            <img v-if="id == 4" src="~/assets/images/7.png" class="image_size">
            <img v-if="id == 5" src="~/assets/images/8.png" class="image_size">
            <img v-if="id == 6" src="~/assets/images/9.png" class="image_size">
            <img v-if="id == 7" src="~/assets/images/10.png" class="image_size">
            <img v-if="id == 8" src="~/assets/images/13.png" class="image_size">
            <img v-if="id == 9" src="~/assets/images/14.png" class="image_size">
            <img v-if="id == 10" src="~/assets/images/15.png" class="image_size">
          </div>   
          <div >
              <router-link>
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
      id: 0
    }
  },
  created() {
    this.fetchData()
  },
  methods: {
    fetchData() {
      const paths_length = 11
      this.id = Math.floor((Math.random()*paths_length))
      console.log(this.id)
    }
  }
};

</script>

<style>
    .margin_bottom {
      margin-bottom:10px;
    }
    .image_size{
      height: 300px;
      width: 600px;
    }
</style>
