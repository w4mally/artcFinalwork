<script setup lang="ts">
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import WarpButton from './components/WarpButton.vue';


interface Place {
    name : string
}

const stt = ref<number>(0)

const index = ref<number>(0)

function myRandom(){
    index.value = 0 + Math.floor( Math.random() * 5 ); 
}

const city = ref<Place[]>([
    { name:'東京' },
    { name:'名古屋' },
    { name:'大阪' },
    { name:'博多' }
])

const nature = ref<Place[]>([
  { name:'沖縄の海' },
  { name:'ひたち海浜公園' },
  { name:'マルーン・ベルズ' },
  { name:'雲海テラス' }
])

const heri = ref<Place[]>([
  { name:'原爆ドーム' },
  { name:'厳島神社' },
  { name:'万里の長城' },
  { name:'マチュピチュ' }
])

</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="芸術C 最終作品 どこでもドア" />
    </div>
  </header>

  <main>
    <WarpButton msg="大都会へ" @click="myRandom();stt = 1" />
    <br>
    <br>
    <WarpButton msg="自然の中へ" @click="myRandom();stt = 2" />
    <br>
    <br>
    <WarpButton msg="世界遺産へ" @click="myRandom();stt = 3" />
    <br>
    <iframe v-if="stt == 0"
    src="https://www.google.com/maps/embed?pb=!4v1721863981418!6m8!1m7!1s7-5yQ4usCbUxzfvw15eMUA!2m2!1d35.60571204801207!2d139.6832731214612!3f276.5598594256122!4f-0.2816861988002586!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 1 && index == 0
    " src="https://www.google.com/maps/embed?pb=!4v1721863509632!6m8!1m7!1sOTx4gPNnY9PXl2KQNGKbqQ!2m2!1d35.68159424408731!2d139.7656192894522!3f109.60155251756346!4f-0.7134488364507945!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 1 && index == 1"
    src="https://www.google.com/maps/embed?pb=!4v1721864117231!6m8!1m7!1s_jZLnQKt7XjkDVKLglextQ!2m2!1d35.17053264140672!2d136.8800809432562!3f247.50296015386047!4f9.138546683293043!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 1 && index == 2"
    src="https://www.google.com/maps/embed?pb=!4v1721864307998!6m8!1m7!1s7ksTbl8b1t4kWBQlQV7tGQ!2m2!1d34.6692881546499!2d135.5012805045377!3f177.47450996199308!4f11.043896767396404!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 1 && index == 3"
    src="https://www.google.com/maps/embed?pb=!4v1721864403106!6m8!1m7!1sj-62p-UA-wCVRS3iHS6xTg!2m2!1d33.58969459870873!2d130.4188227188925!3f189.3336208907713!4f15.291754710976008!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 2 && index == 0"
    src="https://www.google.com/maps/embed?pb=!4v1721864695013!6m8!1m7!1sE1H-R6f5YkLZLdL_9EWrtg!2m2!1d26.69842087644483!2d127.8772127697005!3f300.55150324699736!4f4.484279011343219!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 2 && index == 1"
    src="https://www.google.com/maps/embed?pb=!4v1721865003606!6m8!1m7!1s5V9C6koeno8FZL052RKdzw!2m2!1d36.40448024283413!2d140.6014148884463!3f349.4067455643082!4f6.225326560424463!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 2 && index == 2"
    src="https://www.google.com/maps/embed?pb=!4v1721865147383!6m8!1m7!1sCAoSLEFGMVFpcFBnejVjc0wzNU5wSEFnSExtenVUczRTX2l5MEFkVmtKVEptbW9y!2m2!1d39.07083302018344!2d-106.9888890082776!3f215.8811762943722!4f24.72796186717457!5f0.4000000000000002" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 2 && index == 3"
    src="https://www.google.com/maps/embed?pb=!4v1721865331153!6m8!1m7!1sCAoSLEFGMVFpcE5wb3Q2QTZJM0ZJMWg3czJZSkItakFYdUlWSVExREhaaWNnckN5!2m2!1d43.07490542800372!2d142.5991754755009!3f140.26832634434493!4f8.056183156348524!5f0.5970117501821992" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 3 && index == 0"
    src="https://www.google.com/maps/embed?pb=!4v1721865440700!6m8!1m7!1sSghUHoWukgHIO8GuD0TuEQ!2m2!1d34.39541690139183!2d132.4538534380291!3f293.21234990428223!4f10.287437219869702!5f0.4000000000000002" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 3 && index == 1"
    src="https://www.google.com/maps/embed?pb=!4v1721865516296!6m8!1m7!1sCAoSLEFGMVFpcE1ERTg4eFFNdUdBc3o0OTNndlpQSFNQckJ6Wk4zUVI4U3Qtc25B!2m2!1d34.2959584!2d132.3198506!3f299.7337287748602!4f8.530551782483016!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 3 && index == 2"
    src="https://www.google.com/maps/embed?pb=!4v1721865652176!6m8!1m7!1sCAoSLEFGMVFpcE5mTmJtMUNZRDhqTlJCNHV2Ym56R004STVuNE1lZmRhZldua3Np!2m2!1d40.4409927!2d116.5589562!3f294.79336622986654!4f-9.782519311406062!5f0.7820865974627469" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <iframe v-if="stt == 3 && index == 3"
    src="https://www.google.com/maps/embed?pb=!4v1721865768684!6m8!1m7!1svwDcE5TzKdbsYpq9sa2xxA!2m2!1d-13.1650869094137!2d-72.54470275630072!3f355.05!4f2.5!5f0.4000000000000002" width="400" height="300" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <h1 v-if="stt == 0">どこに行こうかな...</h1>
    <h1 v-if="stt == 1">行先 : {{ city[index].name }}</h1>
    <h1 v-if="stt == 2">行先 : {{ nature[index].name }}</h1>
    <h1 v-if="stt == 3">行先 : {{ heri[index].name }}</h1>
  </main>
</template>