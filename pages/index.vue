<template>
  <v-row justify="center" align="center">
    <v-col  cols="12" sm="8" md="6">
      <div class="text-center margin_bottom">
        <img src="~/assets/images/1.png"/>
      </div>
      <div class="text-center" >
        <v-card class="text-center justify-center">
          <v-card-title class="heacdline justify-center">
            신이 나를 만들 때
          </v-card-title>
          <div justify="center" align="center">
            <v-text-field 
              label="이름"
              placeholder="이름을 입력해주세요"
              class="witdh_50"
              outlined
              rows="1"
              row-height="10"
              v-model="text_value"
              >
            </v-text-field>
          </div>
          <v-card-text>
            입력하신 정보는 본 퀴즈 이외의 용도로 사용하지 않습니다.
          </v-card-text>
          <v-card-actions class="justify-center">
            <div v-if="text_value.length > 1">

              <router-link :to="{name:'result', params:{text_value:text_value}}">
                <v-btn
                  class="margin_bottom"
                  color="primary"
                  nuxt
                >
                  검사하기
                </v-btn>
              </router-link>
            </div>
            <div v-else>
              <v-btn
                  class="margin_bottom"
                  color="primary"
                  nuxt
                  @click="to_result_page"
                >
                  검사하기
                </v-btn>
            </div>
            
          </v-card-actions>
        </v-card>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "index",
  data () {
    return {
      counter: 0,
      text_value:'',
      text:1
    }
  },
  methods: {
    to_result_page: function(event) {
        alert("한 글자라도 입력해주세요")
    },
  }
};

</script>

<style>
    .witdh_50 {
      width:50%
    }
    .witdh_50 input{
      text-align: center;
    }
    .margin_bottom {
      margin-bottom:10px
    }
    
</style>
