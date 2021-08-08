<template>
    <div class="top-comp" > 
        <div class="top container">
            <h1 class="top-title">
                Мобильная партнерская сеть
            </h1>

            <p class="top-text">
               Мы прямой рекламодатель с собственными офферами, которые входят в топ-чарты AppStore и Google Play. 
            </p>

            <div class="topboard d-flex justify-content-center">
                <div class="topboard-item" v-for="(item, index) in top" :key="index">
                    <h3 class="topboard-item__title">
                    {{ item.title }}
                </h3>

                <p class="topboard-item__text">
                    {{ item.text }}
                </p>
                </div>
            </div>

           
        </div>
    </div>
</template>

<script>
export default {
    name:'Set',
props: [
        "top"
    ]
}
</script>

<style lang="scss">


.top-comp{
    position: relative;
    height: 750px;
    background-image: url('../assets/topBack.png') ;
    height: 150% !important;
    background-size: cover;
    


.top{
    padding-top: 105px;
    &-title{
        font-weight: 900;
        font-size: 30px;
        line-height: 37px;
        text-align: center;
        text-transform: uppercase;
        color: #FFFFFF;
        padding-top: 171px;
    }

    &-text{
        font-weight: 500;
        font-size: 20px;
        line-height: 24px;
        color: #FFFFFF;
        max-width: 750px;
        margin: 0 auto;
        text-align: center;
    }

    .topboard{
        
        align-items: flex-start;
        &-item{
            max-width: 350px;
            padding: 51px 0;
            width: 100%;
            margin: 0 16px;
            
            &__title{
                font-weight: 900;
                font-size: 60px;
                line-height: 75px;
                text-align: center;
                color: #FFFFFF;
            }

            &__text{
                font-weight: bold;
                font-size: 16px;
                line-height: 19px;
                text-align: center;
                color: #FFFFFF;
            }
        }
    }

}
}

@media screen and (max-width:760px){
    .top{
        &__title{
         padding-top: 22px !important;
        }
    }
    .topboard{
        flex-direction: column !important;

        &-item{
            padding:0 !important ;
            margin: 8px 0 !important;
            &__title{
                font-size: 36px !important;
            }

        }
    }
}
</style>