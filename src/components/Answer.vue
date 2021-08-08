<template>
    <div class="answer">
        <div class="container">
           

        <h1 class="answer-title">
            Остались вопросы? Готовы ответить!
        </h1>

        <form action="#" class="answer-form">
            <input class="answer-form__input" type="text" placeholder="Ваше имя" required><br>
            <input class="answer-form__input" type="text" placeholder="Ваши контакты" required><br>
            <input class="answer-form__input" type="text" placeholder="Ваше предложения" required><br>
            <input  class="answer-form__submit" type="submit" value="написать нам">
        </form>
        </div>
    </div>
</template>

<script>
export default {
    name:'Answer',
}
</script>

<style lang="scss">
.answer{
    margin-top: 108px;
    height: 750px;
    background-image: url('../assets/answerBack.png') ;
    background-repeat: no-repeat;
    padding: 128px 0;
   
    
    &-title{
        font-weight: 900;
        font-size: 30px;
        line-height: 37px;
        text-align: center;
        color: #FFFFFF;
    }

    &-form{
        text-align: center;
        margin: 30px 0;

        &__input{
            background: #FFFFFF;
            border: none;
            outline: none;
            padding: 28px 30px;
            border-radius: 40px;
            margin: 10px 0;
            max-width: 750px;
            width: 100%;
            font-weight: 500;
            font-size: 20px;
            line-height: 24px;
            color: rgba(126, 126, 126, 0.5);
        }

        &__submit{
            max-width: 350px;
            width: 100%;
            text-align: center;
            padding: 28px 30px;
            background: transparent;
            border: 1px solid white;
            font-weight: 900;
            font-size: 20px;
            line-height: 24px;
            text-align: center;
            text-transform: uppercase;
            color: #FFFFFF;
            border-radius: 40px;
            margin-top: 30px;
            cursor: pointer;
            

            &:hover{
                background: linear-gradient( rgba(81, 243, 176, 0.8), rgba(255,0,0,0) ),
                linear-gradient( #55B570, rgba(0,255,0,0) ),
                linear-gradient( #2E9ADB, rgba(0,0,255,0) );
                transition: all 0.3s;
            }
        }
    }


}
</style>