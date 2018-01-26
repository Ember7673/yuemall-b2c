<template>
    <div>
        <div class="des-body">
            <ul>
                <li v-for="(item,i) in destination" :key="i">
                <span>{{item.title}}：</span>
                <ul class="des-list">
                    <li>
                    <a href="#" v-for="(i,index) in item.city" :key="index">{{i}}</a>
                    </li>
                </ul>
                </li>
            </ul>
        </div>
    </div>    
</template>

<script>
export default {

    data() {
        return{
            destination: [
                {
                title: '热门',
                city: ['三亚','厦门','丽江','大理','巴厘岛','罗马','皇后镇','悉尼']
                },
                {
                title: '国内',
                city: ['北京','三亚','北京','三亚','北京','三亚','北京','三亚','高雄','垦丁']
                },
                {
                title: '欧洲',
                city: ['巴黎','普罗旺斯','罗马','巴黎','普罗旺斯','罗马','巴黎','普罗旺斯','罗马','巴黎','普罗旺斯','苏黎世']
                },
                {
                title: '亚洲',
                city: ['普吉岛','苏海岛','巴厘岛','普吉岛','苏海岛','巴厘岛','普吉岛','苏海岛','巴厘岛','普吉岛','苏海岛','巴厘岛']
                },
                {
                title: '大洋洲',
                city: ['奥克兰','皇后镇','基督城','墨尔本','悉尼']
                },
                {
                title: '美洲',
                city: ['塞班','洛杉矶']
                }
            ],
        }
    },
    
};
</script>

<style lang="scss" scoped>
$color: #19A9E8;
.des-body {
  margin-top: 45px;
  ul {
    list-style: none;
    -webkit-padding-start: 0;
    li {
      display: flex;
      margin-top: 20px;
      flex-wrap: wrap;
      margin-left: 300px;
      span {
        color: $color;
        font-size: 14px;
      }
      .des-list {
        display: inline;
        li {
          margin: 0;
          a {
            border: 1px solid #888;
            color: #888;
            padding: 3px 6px;
            border-radius: 4px;
            margin-left: 5px;
            margin-bottom: 5px;
            font-size: 12px;
          }
        }
      }
    }
  }
}
</style>
