<template>
    <div class="set-comp" >
        
        <Particles class="particles"
            id="tsparticles"
            :particlesInit="particlesInit"
            :particlesLoaded="particlesLoaded"
            :options="option"
        />
        
        <div class="set container">
            <h1 class="set-title">
                Мобильная партнерская сеть
            </h1>

            <p class="set-text">
                Только рабочие офферы от прямых рекламодателей
            </p>

            <div class="dashboard d-flex align-items-center justify-content-center">
                <div class="dashboard-item" v-for="(item, index) in dashboard" :key="index">
                    <h3 class="dashboard-item__title">
                    {{ item.title }}
                </h3>

                <p class="dashboard-item__text">
                    {{ item.text }}
                </p>
                </div>
            </div>

            <div class="inform d-flex align-items-center justify-content-between">
                <div class="inform-item">
                    <p class="inform-item__text">
                        Я пользователь соцсетей, блогер, владелец сайта или арбитражник и хочу сотрудничать с топовыми мировыми брендами.
                    </p>

                    <button class="inform-item__btn btn">
                        веб-мастерам
                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <g clip-path="url(#clip0)">
                            <path d="M10.553 19.7709C10.5532 19.7706 10.5535 19.7704 10.5538 19.7702L14.6163 15.688C14.9206 15.3821 14.9195 14.8875 14.6136 14.5831C14.3078 14.2787 13.8131 14.2799 13.5088 14.5857L10.7813 17.3265L10.7813 0.78125C10.7813 0.349765 10.4315 -1.92866e-07 10 -2.11727e-07C9.56852 -2.30588e-07 9.21875 0.349765 9.21875 0.78125L9.21875 17.3264L6.49125 14.5857C6.18688 14.2799 5.69223 14.2788 5.38641 14.5831C5.08051 14.8875 5.07945 15.3822 5.38375 15.688L9.44625 19.7702C9.44649 19.7704 9.44676 19.7706 9.44699 19.7709C9.75238 20.0769 10.2486 20.0759 10.553 19.7709Z" fill="white"/>
                            </g>
                            <defs>
                            <clipPath id="clip0">
                            <rect width="20" height="20" fill="white" transform="translate(20) rotate(90)"/>
                            </clipPath>
                            </defs>
                        </svg>
                    </button>
                </div>

                <div class="inform-item">
                    <p class="inform-item__text">
                        Я владелец компании или маркетолог и хочу привлечь новых клиентов и увеличить продажи с помощью онлайн-рекламы.
                        </p>
                    <button class="inform-item__btn  btn">
                        рекламодателю
                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <g clip-path="url(#clip0)">
                            <path d="M19.7709 9.44699C19.7706 9.44676 19.7704 9.44648 19.7702 9.44625L15.688 5.38375C15.3821 5.07941 14.8875 5.08054 14.5831 5.3864C14.2787 5.69222 14.2799 6.18687 14.5857 6.49125L17.3265 9.21875H0.78125C0.349766 9.21875 0 9.56851 0 10C0 10.4315 0.349766 10.7812 0.78125 10.7812H17.3264L14.5857 13.5087C14.2799 13.8131 14.2788 14.3078 14.5831 14.6136C14.8875 14.9195 15.3822 14.9205 15.688 14.6162L19.7702 10.5537C19.7704 10.5535 19.7706 10.5532 19.7709 10.553C20.0769 10.2476 20.0759 9.75137 19.7709 9.44699Z" fill="white"/>
                            </g>
                            <defs>
                            <clipPath id="clip0">
                            <rect width="20" height="20" fill="white"/>
                            </clipPath>
                            </defs>
                        </svg>

                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name:'Set',


data (){
    
        
      
    return{
      option : {
        background: {
          color: {
            value: 'transparent'
          }
        },
        fpsLimit: 60,
        interactivity: {
          detectsOn: 'canvas',
          events: {
            onClick: {
              enable: true,
              mode: 'push'
            },
            onHover: {
              enable: true,
              mode: 'repulse'
            },
            resize: true
          },
          modes: {
            bubble: {
              distance: 400,
              duration: 2,
              opacity: 0.8,
              size: 40
            },
            push: {
              quantity: 4
            },
            repulse: {
              distance: 200,
              duration: 0.4
            }
          }
        },
        particles: {
          color: {
            value: '#ffffff'
          },
          links: {
            color: '#ffffff',
            distance: 150,
            enable: true,
            opacity: 0.5,
            width: 1
          },
          collisions: {
            enable: true
          },
          move: {
            direction: 'none',
            enable: true,
            outMode: 'bounce',
            random: false,
            speed: 6,
            straight: false
          },
          number: {
            density: {
              enable: true,
              value_area: 800
            },
            value: 80
          },
          opacity: {
            value: 0.5
          },
          shape: {
            type: 'circle'
          },
          size: {
            random: true,
            value: 5
          }
        },
        detectRetina: true
      }
    }
  },

props: [
        "dashboard"
    ]
}
</script>

<style lang="scss">
.set-comp{
    position: relative;
    height: 750px;
    background-image: url('../assets/setBack.jpg') ;
    background-size: cover;
    height: 100%;
    
.set-back{
    width: 100%;
}
.particles{
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    z-index: 0;
}

.set{


    &-title{
        font-weight: 900;
        font-size: 60px;
        line-height: 75px;
        text-align: center;
        text-transform: uppercase;
        color: #FFFFFF;
        padding-top: 171px;
    }

    &-text{
        font-weight: 500;
        font-size: 20px;
        line-height: 24px;
        text-align: center;
        color: #FFFFFF;
    }

    .dashboard{
        margin-top: 70px;
        &-item{
            border-right:1px solid white;
            max-width: 276px;
            padding: 51px 0;
            width: 100%;
            
            &:last-child{
                border: none !important;
            }
            &__title{
                font-size: 40px;
                line-height: 49px;
                text-align: center;
                color: #FFFFFF;
            }

            &__text{
                font-weight: 500;
                font-size: 16px;
                line-height: 19px;
                text-align: center;
                color: #FFFFFF;
            }
        }
    }

    .inform{
        position: relative;
        background: #FFFFFF;
        box-shadow: 0px 20px 80px rgba(0, 0, 0, 0.08);
        border-radius: 8px;
        max-width: 1100px;
        margin: 0 auto;
        

        &-item{
            padding: 58px 50px;
            text-align: center;
            &__text{
                font-weight: 500;
                font-size: 16px;
                line-height: 24px;
                text-align: center;
                color: #000000;
            }

            &__btn{
                background: #2E9ADB;
                box-shadow: 0px 10px 20px rgba(78, 170, 224, 0.35);
                border-radius: 40px;
                font-weight: 900;
                font-size: 20px;
                line-height: 24px;
                text-align: center;
                text-transform: uppercase;
                color: #FFFFFF;
                padding: 28px 30px 28px 62px;
                cursor: pointer;

                svg{
                    margin-left: 16px;;
                }

                &:hover{
                    background-color: #55B570;
                    transition: all 0.3s;
                }
            }
      }
    }
    
}
}

@media screen and (max-width:1190px) {
  .set{
    &-title{
      font-size: 36px ;
    }

    &-text{
      font-size: 16px !important;
    }
  }
 
  
}

@media screen and (max-width:880px){

.set-comp{
.set{


    &-title{
        font-weight: 700;
        font-size: 28px;
        line-height: 35px;
        padding-top: 102px;
    }

    &-text{
        font-weight: 400;
        font-size: 16px;
        line-height: 14px;
    }
}
}}

@media screen and (max-width:760px){

  .set-comp{
    .set{


      &-title{
        font-weight: 700;
        font-size: 28px;
        line-height: 35px;
        padding-top: 102px;
      }

      &-text{
        font-weight: 400;
        font-size: 16px;
        line-height: 14px;
      }

      &-inform{
        
        flex-direction: column;
      }
    }
  }

  .dashboard{
        margin-top: 30px;
        justify-content: center !important;
        display: grid !important; 
        grid-template-columns: 1fr 1fr;
        &-item{
            border-right:1px solid white;
            max-width: 276px;
            margin: 0 auto;
            padding: 31px 0;
            width: 100%;
            
            &:nth-last-child(3){
              border-right: none !important;
                border-bottom:1px solid white !important;
                border-width: 100%;
            }
            &:nth-last-child(4){
                border-bottom:1px solid white !important;
                border-width: 100%;
            }
           
        }
    }

    .inform{
        margin: 0 auto;
        flex-direction: column ;
        &-item{
            padding: 58px 50px;
            text-align: center;
            &__text{
                font-weight: 500;
                font-size: 16px;
                line-height: 24px;
                text-align: center;
                color: #000000;
            }

            &__btn{
                background: #2E9ADB;
                box-shadow: 0px 10px 20px rgba(78, 170, 224, 0.35);
                border-radius: 40px;
                font-weight: 900;
                font-size: 20px;
                line-height: 24px;
                text-align: center;
                text-transform: uppercase;
                color: #FFFFFF;
                padding: 28px 30px 28px 62px;
                cursor: pointer;

                svg{
                    margin-left: 16px;;
                }

                &:hover{
                    background-color: #55B570;
                    transition: all 0.3s;
                }
            }
      }
    }

}
</style>