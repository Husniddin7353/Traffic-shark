<template>
    <div class="vertical">
        <div class="container">
            <h1 class="vertical-title">
                Топовые вертикали
            </h1>

            <div class="vertical-blog">
                <div class="vertical-blog__item" v-for="(item, index) in vertical" :key="index">
                    <img :src="item.img" alt="" class="item-img">
                     
                    <p class="item-title">
                        {{ item.title }}
                    </p>
                    <p class="item-text">
                        {{ item.text }}
                    </p>
                </div>
            </div>

        
        </div>
    </div>
</template>

<script>
export default {
    name:'Vertical',

    props: [
        "vertical"
    ]
}
</script>
<style lang="scss">
.vertical{
    margin: 80px 0;
    text-align: center;
    &-title{
        font-weight: 900;
        font-size: 30px;
        line-height: 37px;
        text-align: center;
        text-transform: uppercase;
        color: #000000;
        margin: 60px 0;
    }

    &-blog{
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        

        &__item{
            text-align: start;
            padding: 20px;
            max-width: 350px;
            margin: 0 auto;
            width: 100%;
            cursor: pointer;
            &:hover{
                box-shadow: 0px 20px 80px rgba(0, 0, 0, 0.08);
                border-radius: 8px;
                transition: all 0.3s;
            }

            .item-img{
                margin-bottom: 30px;
            }

            .item-title{
                font-weight: 900;
                font-size: 20px;
                line-height: 25px;
                color: #000000;
                margin-top: -60px;
                padding: 0 40px;
            }
            .item-text{
                font-weight: 300;
                font-size: 14px;
                line-height: 16px;
                text-align: start;
                color: #000000;
                padding: 0 40px;
                max-width: 350px;
                width: 100%;
            }

            

            
        }
    }

  
    
}
</style>