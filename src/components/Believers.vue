<template>
    <div class="believer">
        <div class="container">
            <h1 class="believer__title">
                Еженедельные выплаты <span> от $100</span>
            </h1>

            <p class="believer__text">
                На удобную для вас платежную систему из перечисленных ниже
            </p>

            <div class="believer-blog align-items-center ">
                <img src="@/assets/l1.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l2.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l3.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l4.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l5.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l6.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l7.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l8.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l9.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l10.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l11.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l12.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l13.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l14.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/l16.png" alt="" class="withdraw-blog__img">

            </div>


        </div>
    </div>
</template>

<script>
export default {
    name:'Believer'
}
</script>

<style lang="scss">
.believer{
    &__title{
        font-weight: 900;
        font-size: 30px;
        line-height: 37px;
        text-align: center;
        text-transform: uppercase;
        color: #000000;
    }

    &__text{
        font-weight: 500;
        font-size: 20px;
        line-height: 24px;
        text-align: center;
        color: #939393;
    }

    &-blog{
        margin-top: 88px;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 50px ;

        &__img{
            cursor: pointer;    
        }
    }
}
</style>