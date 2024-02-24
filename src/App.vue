<template>

  <v-app>
  <AppHeader > </AppHeader>
    <v-main>
    <!-- Hero Section -->
    <HeroComponent ></HeroComponent>
        <!-- About Us -->
    <AboutUs></AboutUs>
        <!-- OzelliklerR-->
    <OzelliklerR></OzelliklerR>
           <!--ResimM-->
           <ResimM></ResimM>

        <!--Hakkimizda-->
    <HakkimizDa></HakkimizDa> 

        <!-- Contact us-->         
    <ContactUs></ContactUs>
    <!--Footer-->
     <FooterR></FooterR>

               



  

    </v-main>
  </v-app>
</template>
<script>
import AppHeader from "./components/Header.vue";
import HeroComponent from "./components/HeroComponent.vue";
import AboutUs from "./components/AboutUs";
import OzelliklerR from './components/OzelliklerR.vue';
import ContactUs from './components/ContactUs.vue';
import HakkimizDa from './components/HakkimizDa.vue';
import FooterR from "./components/FooterR.vue";
import ResimM from "./components/ResimM.vue";
//import HelloWorld from './components/HelloWorld';


export default {
    name: "App",
    components: {AboutUs,HeroComponent,AppHeader,ResimM ,OzelliklerR,ContactUs, HakkimizDa,FooterR},

    data(){
      return{
        menus:[
          {title:"Perfx",route:"perfx"},
          {title:"Özellikler",route:"özellikler"},
          {title:"Hakkımızda",route:"hakkımızda"},
          {title:"Bize Ulaşın",route:"bize-ulaşın"},
          {title:"Perfx",route:"perfx"},

        ]
      }

      
    },
};
</script>
