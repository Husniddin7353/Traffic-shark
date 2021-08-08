<template>
    <div class="withdraw">
        <div class="container">
            <h1 class="withdraw__title">
                Еженедельные выплаты <span> от $100</span>
            </h1>

            <p class="withdraw__text">
                На удобную для вас платежную систему из перечисленных ниже
            </p>

            <div class="withdraw-blog d-flex align-items-center justify-content-between">
                <img src="@/assets/z1.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/z2.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/z3.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/z4.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/z5.png" alt="" class="withdraw-blog__img">
                <img src="@/assets/z6.png" alt="" class="withdraw-blog__img">
            </div>


        </div>
    </div>
</template>

<script>
export default {
    name:'Withdraw'
}
</script>

<style lang="scss">
.withdraw{

    
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
        flex-wrap: wrap;
        gap: 20px;

        &__img{
            cursor: pointer;
        }
    }
}
</style>