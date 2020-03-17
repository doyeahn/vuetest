 <style>
.score {
  border: solid 1px black;
}
.warning {
  background-color: orange;
  color: purple;
}
.warnimage {
  width: 18px;
  height: 18px;
  top: 5px;
  position: relative;
}
</style>

<template>
  <div id="search">
    <div>
      입력:
      <input type="text" class="score" v-model="player" />
      <img src="assets/error.jpg" class="warnimage" v-show="info.warning" />
    </div>
  </div>
</template>
    <!--    <script src="https://unpkg.com/vue@2.5.16/dist/vue.js"></script>
 --> 

<script>
export default {
  name: "search",
  data: function(){
      return {player:''}
  },
  computed:
{
    info: function(){
            if(this.player === 'seungwoolee')
            return { waring : true};
            else return {warning : false};
}
}
}
</script>
