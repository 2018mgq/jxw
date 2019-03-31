<template>
    <div id="tabber">
        </router-view>

        <ul class="tabbers">
            <router-link 
            tag="li"
            :to="item.path" 
            v-for="(item,index) in tabber"
            >
                <i class="iconfont" v-html="item.icon"></i>
                <h2>{{item.title}}</h2>
            </router-link>
            <!-- <router-link tag="li" to="/classification">
                <i></i>
                <h2>分类</h2>
            </router-link>
            <router-link tag="li" to="/reservations">
                <i></i>
                <h2>我要预定</h2>
            </router-link>
            <router-link tag="li" to="/shopping">
                <i></i>
                <h2>购物车</h2>
            </router-link>
            <router-link tag="li" to="/mine">
                <i></i>
                <h2>我的</h2>
            </router-link> -->

        </ul>
    </div>
</template>
<script>
export default {
    name:"tabber", 
    data() {
        return {
            tabber:[
                {
                    title:"首页",
                    path:"/page",
                    icon:"&#xe61d;"
                },
                {
                    title:"分类",
                    path:"/classification",
                    icon:"&#xe602;"
                },
                {
                    title:"我要预定",
                    path:"/reservations",
                    icon:"&#xe81b;"
                },
                {
                    title:"购物车",
                    path:"/shopping",
                    icon:"&#xe501;"
                },
                {
                    title:"我的",
                    path:"/mine",
                    icon:"&#xe622;"
                },

            ]
        }
    }
}
</script>
<style scoped lang="scss">
    #tabber{
        width:100%;
        height:1rem;
        position:fixed;
        background:#fff;
        left:0;
        bottom:0;
        border-top:1px solid #333;
        .tabbers{
            width:100%;
            height:100%;
            display:flex;
            justify-content:space-between;
            align-items:center;
            li{
                width:100%;
                height:100%;
                display:flex;
                flex-direction:column;
                justify-content:center;
                color:#333;
                font-size:.2rem;
            }
        }
    }
    #tabber .tabbers .router-link-active{
        color:#c33;
    }
    #tabber .tabbers li h2{
        display:block;
        text-align:center;
        padding-top:.05rem;
    }
    #tabber .tabbers li i{
        font-size:.4rem;
        text-align:center;
    }
</style>