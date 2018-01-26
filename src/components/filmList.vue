<template>
    <div>
        <div class="local-film-body">
            <ul>
            <li :class="[ isthird ? 'is-third' : 'is-second' ]" v-for="(item,i) in filmList" :key="i">
                <img :src="item.img" alt="">
                <p>{{item.title}}</p>
                <span>{{item.pTitle}}</span>
            </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
data() {
    return{

    }
},
props: ['filmList', 'isthird']
}
</script>

<style lang="scss" scoped>
.local-film-body{
        box-sizing: border-box;
        padding: 40px 80px;
        ul{
            li{
                display: inline-block;
                margin-top: 30px;
                padding: 5px;
                img{
                    display: block;
                    width: 100%;
                    height: 100%;
                }
                p{
                padding-top: 24px;
                color: #646464;
                font-size: 16px;
                font-weight: bold;
                }
                span{
                color: #aeaeae;
                font-size: 12px;
                }
            }
            .is-third{
                    width: 32%;
                }
            .is-second{
                width: 49%;
            }
        }
    }

</style>
