<template>
    <div class="withus">
        <div class="container">
            <h1 class="withus-title">
                Работать с нами это
            </h1>

            <div class="withus-blog">
                <div class="withus-blog__item" v-for="(item, index) in work" :key="index">
                    <img :src="item.img" alt="" class="item-img">
                    <p class="item-text">
                        {{ item.text }}
                    </p>
                </div>
            </div>

            <button class="withus-btn btn">Регистрация</button>
        </div>
    </div>
</template>

<script>
export default {
    name:'WithUs',

    props: [
        "work"
    ]
}
</script>
<style lang="scss">
.withus{
    margin: 80px 0;
    text-align: center;
    &-title{
        font-weight: 900;
        font-size: 30px;
        line-height: 37px;
        text-align: center;
        text-transform: uppercase;
        color: #000000;
    }

    &-blog{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;

        &__item{
            text-align: center;
            padding: 20px;
            cursor: pointer;
            &:hover{
                box-shadow: 0px 20px 80px rgba(0, 0, 0, 0.08);
                border-radius: 8px;
                transition: all 0.3s;
            }

            .item-img{
                margin-bottom: 30px;
            }

            .item-text{
                font-weight: 300;
                font-size: 20px;
                line-height: 23px;
                text-align: center;
                color: #000000;
            }

            

            
        }
    }

    &-btn{
        background: linear-gradient(0deg, #FFFFFF, #FFFFFF);
        border: 4px solid #2E9ADB;
        box-sizing: border-box;
        border-radius: 40px;
        font-weight: 900;
        font-size: 20px;
        line-height: 24px;
        text-align: center;
        text-transform: uppercase;
        color: #2E9ADB;
        padding: 28px ;
        max-width: 350px;
        width: 100%;
        margin: 0 auto;

        &:hover{
            color: white;
            background: #2E9ADB;
            transition: all 0.3s;            
        }
    }
}

@media screen and (max-width:1190px){
    .withus{
        &-blog{
            display: grid;
            grid-template-columns: 1fr 1fr;
        }
    }
}
</style>