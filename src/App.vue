<template>
  <div id="app">
      
      <Header/>
    

      <Set :dashboard="dashboard" :title="dashboard.title" :text="dashboard.text" />
      <WithUs :work="work" :img="work.img" :text="work.text" />
      <Top :top="top" :img="top.img" :text="top.text" />
      <Withdraw/>
      <Vertical :vertical="vertical" :img="vertical.img"  :text="vertical.text" />
      <Believer/>
      <Answer/>
      <Footer/>
        
      
  </div>
</template>

<script>

import Header from '@/components/Header.vue'
import Set from '@/components/Set.vue'
import WithUs from '@/components/WithUs.vue'
import Top from '@/components/Top.vue'
import Withdraw from '@/components/Withdraw.vue'
import Vertical from '@/components/Vertical.vue'
import Believer from '@/components/Believers.vue'
import Answer from '@/components/Answer.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: "App",
  components:{
    Header,
    Set,
    WithUs,
    Top,
    Withdraw,
    Vertical,
    Believer,
    Answer,
    Footer
  },
  data () {
    return {
       
      dashboard:[
        {
          title: '300+',
          text: 'офферов по всему миру'
        },

        {
          title: '70+',
          text: 'активных рекламодателей'
        },

        {
          title: '6 ЛЕТ',
          text: 'в аффилейт маркетинге'
        },

        {
          title: '10.000+',
          text: 'конверсий в день'
        }
      ],

      top:[
        {
          title: 'ТОП',
          text: 'Наши офферы входят в ТОПы в AppStore и Google Play'
        },

        {
          title: 'ОФФЕРИ',
          text: 'Мы делаем собственные белые мобильные офферы, которые вы не найдете ни в одной другой партнерке'
        },

        {
          title: '2.5S',
          text: 'Мы платим до $2.5 за инсталл и принимаем трафик со всего мира'
        }
      ],

      work:[
        { img: require('@/assets/withus1.png') ,
          text: 'Уверенность и стабильность! Мы на рынке с 2015г. '},

        { img: require('@/assets/withus2.png'),
          text: 'Большой выбор мобильных приложений и аддонов ' },

        { img: require('@/assets/withus3.png'),
          text: 'Дружелюбная и квалифицированная поддержка ' },

        { img: require('@/assets/withus4.png'),
          text: 'Эффективная монетизация Pop-under, Push, In-App, FB, Google и других источников трафика ' },

        { img: require('@/assets/withus5.png'),
          text: 'Эксклюзивные предложения благодаря собственному сильному баингу ' },

        { img: require('@/assets/withus6.png'),
          text: 'Стабильные выплаты 1 раз в неделю от $100 после проверки качества ' },

      ],

       vertical:[
        { img: require('@/assets/v1.png') ,
          title: 'Installs',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna. '},

        { img: require('@/assets/v2.png'),
          title: 'Utilities',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna. ' },
          
        { img: require('@/assets/v3.png'),
          title: 'APK',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna. ' },

        { img: require('@/assets/v4.png'),
          title: 'Addons',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna. ' },
         
        { img: require('@/assets/v5.png'),
          title: 'Gambling/Betting ',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.' },

        { img: require('@/assets/v6.png'),
          title: 'Новые вертикали',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.' },

      ]
    }
  }
}

</script>

<style lang="scss">


.container{
  max-width: 1190px;
  margin: 0 auto;
}

a{
  text-decoration: none;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

</style>
