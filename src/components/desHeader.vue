<template>
  <div>
      <div class="des-header w">
            <p>{{headerTitle}}</p>
            <p>{{headerPtitle}}</p>
            <div class="header-box"></div>
          </div>
  </div>
</template>

<script>
export default {
data() {
  return{

  }
},
props: ['headerTitle', 'headerPtitle']
}
</script>

<style lang="scss" scoped>
$color: #19A9E8;
.des-header{
    position: relative;
    border-bottom: 1px solid #eee;
    margin-top: 70px;
    padding: 30px;
    p{
      text-align: center;
      font-size: 35px;
      font-weight: bold;
      color: $color;
      letter-spacing: 3px;
      margin: 0;
    }
    p:nth-child(2){
      font-size: 12px;
      font-weight: normal;
      letter-spacing: 1px;
    }
    .header-box{
      width: 70px;
      height: 5px;
      background-color: $color;
      position: absolute;
      left: 50%;
      bottom: 0;
      transform: translateX(-50%);
    }
}

</style>
