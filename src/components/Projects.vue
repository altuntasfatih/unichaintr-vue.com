<template>
  <div class="block3">
    <div class="fixed-bg bg1"></div>
    <div class="container">
      <div class="building-gallery-tab">
        <div class="gallery-tabs-head">
          <h4>"{{$t("motto")}}"</h4>
        </div><!--gallery-tabs-head end-->
        <div class="gallery-tab-contents">
          <div class="row ">
            <div class="col-lg-4 col-md-8">
              <div class="locations-images">
                <div class="location-img current" id="tab-1">
                  <a href="https://github.com/Unichain-turkey/ether-registration" target="_blank"><img src="static/images/registhereum.svg" alt=""></a>

                </div><!--location-img end-->
                <div class="location-img " id="tab-2">
                  <a href="https://github.com/Unichain-turkey/adhereum" target="_blank"><img src="static/images/adhereum.svg" alt=""></a>
                </div><!--location-img end-->
              </div><!--locations-images end-->
            </div>

            <div class="col-lg-4 col-md-8 ">
              <div class="locations-info">
                <div class="location-info current " id="tab-1" >
                  <p class="pt-2 ">{{info}}</p>
                  <router-link :to="{ path: 'demo' }">Demo</router-link>
                </div>

              </div><!--locations-images end-->
            </div>
            <div class="col-lg-4 col-md-4">
              <div class="locations-list">
                <ul>
                  <li @click="tabClick(1)" class="current" data-tab="tab-1">Registhereum</li>
                  <li  @click="tabClick(2)"  data-tab="tab-2">Adhereum</li>
                </ul>
              </div><!--locations-list end-->
            </div>
          </div>
        </div><!--gallery-tab-content end-->
      </div><!--building-gallery-tab end-->
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data () {
    return {
      info:this.$t("registereum")

    }
  },
  methods:{
    tabClick:function (index) {
      console.log(index)
      if (index==1){
        this.info=this.$t("registereum")
      }
      else{
        this.info=this.$t("adhereum")
      }


    }
  }

}
</script>

<style scoped>

</style>
