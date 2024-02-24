<template>
    <v-app-bar
    style="padding: 0px 90px"
      app
      color="#344199 "
      light
      elevation="6"
      elevate-on-scroll

    >
    <v-toolbar-title ><img src="./../assets/main-logo.png" alt=""></v-toolbar-title>
    <v-spacer />
   <v-list class="d-flex align center"> 
      <v-list-item link v-for="(menu,index) in menus" :key="index" :to="menu.route">
        <v-list-item-title>{{menu.title}}</v-list-item-title>
      </v-list-item>
      <v-btn text>
        <v-icon>mdi-earth <p>En</p></v-icon>
      </v-btn>
      <v-btn    color="success" class="white--text " rounded>GİRİŞ</v-btn>
    </v-list>

     </v-app-bar>
</template>

<script>
   export default {
    name: "AppHeader",
    data(){
      return{
        menus:[
         // <style color='blue'></style>,
          {title:"Perfx"         ,route:"perfx"},
          {title:"Özellikler"    ,route:"özellikler"},
          {title:"Hakkımızda"    ,route:"hakkımızda"},
          {title:"Bize Ulaşın"   ,route:"bize-ulaşın"},
          {title:"Perfx"         ,route:"perfx"},


        ]
      }

      
    },
   }


</script>
<style scoped>
.v-toolbar__title {
    font-size: 40px;
    color: brown;
    font-weight: 900;
    font-family: system-ui;
}
.v-list.d-flex.align.center.v-sheet.theme--light {
    background: bottom;
}
.v-toolbar__content {
    background-color: #344199;
}

.theme--light.v-list-item:not(.v-list-item--active):not(.v-list-item--disabled) {
    color: rgb(255 255 255 / 87%);
}
.v-list-item__title {
    align-self: center;
    font-size: 17px;
    font-weight: 600;
    font-family: sans-serif;
}

</style>
