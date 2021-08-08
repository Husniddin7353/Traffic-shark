<template>
      <div class="header ">
        <div class="container  ">
          <div class="header-regular d-flex align-items-center justify-content-between">
            <a href="#"><img src="@/assets/logo.png" alt=""></a>

        <nav class="header-nav d-flex align-items-center justify-content-between">
            <div class="nav-res">
              <a href="#" class="header-nav__link">вебмастерам</a>
              <a href="#" class="header-nav__link">рекламодателям</a>
            </div>
            <a href="#" class="header-nav__link header-nav__green ">вход <span class="link-res"> | регистрация</span> </a>
        </nav>
        <form class="form d-flex align-items-start">
              <input
                class="form__input"
                type="radio"
                name="opt"
                id="opt1"
                checked>
              
              <label class="form__lable active" for="opt1">RU</label>
              <input class="form__input" type="radio" name="opt" id="opt2"/>
              <label class="form__lable active" for="opt2">EN</label>
          </form>
          </div>


        <div class="header-res">
          <div class="d-flex align-items-center justify-content-between">
            <a href="#"><img src="@/assets/logo.png" alt=""></a>


            <div class="header-res-nav d-flex align-items-center justify-content-between">
                <a href="#" class="header-nav__link header-nav__green ">вход <span class="link-res"> | регистрация</span> </a>
                <form class="form d-flex align-items-start">
                <input
                  class="form__input"
                  type="radio"
                  name="opt"
                  id="opt1"
                  checked>
                
                <label class="form__lable active" for="opt1">RU</label>
                <input class="form__input" type="radio" name="opt" id="opt2"/>
                <label class="form__lable active" for="opt2">EN</label>
                </form>
            </div>
          </div>

          <div class="nav-res">
              <a href="#" class="header-nav__link">вебмастерам</a>
              <a href="#" class="header-nav__link">рекламодателям</a>
            </div>
        </div>

        </div>

        
    </div>
</template>

<script>


export default {
    name:'Header'
    
}
</script>

<style lang="scss">
.head{
  background-color: white !important;
}
.header{

  &-res{
    display: none;
  }
   position: fixed;
   z-index: 1;
   width: 100%;
   background-color: white;

    &-nav{
        margin-left: 30%;
        &__link{
            font-weight: bold;
            font-size: 13px;
            line-height: 16px;
            text-align: right;
            text-transform: uppercase;
            color: #565656; 
            margin: 0 25px;  
            text-decoration: none !important;
            
            &:hover{
                color:#55B570 ;
                transition: all 0.2s;
            }
        }
        &__green{
           color: #55B570;
           border-right: 1px solid #F4F4F4;
           border-left: 1px solid #F4F4F4;
           padding: 30px 50px;


           &:hover{
               color: white;
               background: #4EAAE0;
               border-radius: 8px;
               transition: all 0.3s;
            }
        }

       
    }
}

.form {
  background: #f9f9f9;
  border: 1px solid #ebebeb;
  box-sizing: border-box;
  border-radius: 14px;
  height: 30px;
  width: 78px;
  display: flex;
  align-items: center;
  justify-content: space-around;

  &__input[type="radio"] {
    display: none;
  }

  &__lable {
    font-style: normal;
    font-weight: bold;
    font-size: 11px;
    line-height: 13px;
    display: flex;
    align-items: center;
    text-align: center;
    color: #797979;
    padding: 8px 10px;
    border-radius: 14px;
  }

  &__input[type="radio"]:checked + &__lable {
    padding: 8px 13.5px;
    color: #fff;
    background-color: #4eaae0;
    transition: all 0.35s ease-in-out;
  }
}

@media screen and (max-width:1190px) {
  .header{
   position: fixed;
   z-index: 1;
   width: 100%;
   background-color: white;

    &-nav{
        margin-left: 10%;

        .link-res{
          display: none;
        }
    }
}

@media screen and (max-width:760px){
   .header{
     width: 100%;
   &-regular{
     display: none !important;
   }

   &-res{
     max-width: 380px;
     margin: 0 auto;
     display: block;
      
     .link-res{
       display: none !important;
     }
    &-nav{
      width: 50% !important;
      margin-right: 20%;
      &__link{

      }
    }
   }
} 
}
}
</style>