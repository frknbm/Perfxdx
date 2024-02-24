<template>
  
    <v-container>
      <v-row justify="center">
        <div class="background">
        <img   src="./../assets/content-image-3.png" alt="" id="oz">              
</div>
  <div class="background" >
    <v-col lg="12" class="text-center">
      <v-subheader class="text-h4">İK Yöneticileri Yeni Nesil Performans Yönetimini Çok Sevecek</v-subheader>
     </v-col>
     <br>                  
  <v-col lg="6" id="ba">
        <v-icon color="success">mdi-check</v-icon>Ortak yetkinlik ve şirket strateji kütüphaneleri <br>
      <v-icon color="success">mdi-check</v-icon>Yetkinlik atama matrisleri <br>
      <v-icon color="success">mdi-check</v-icon>Onay akışları, istisnai onay ve toplu onay işlemleri <br>
      <v-icon color="success">mdi-check</v-icon>Çalışan gruplarına göre farklılaşan performans parametreleri <br>
</v-col>
    </div>         
          </v-row> 
    </v-container>
  
  
  </template>
  <script>
     export default{
      name:"OzelliklerR",
  
     }
  
  
  </script>
  
  <style scoped>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 50vh;
  }
  .background {
    background-color: #344199; 
    padding: 15px 410px  15px  400px;
    border-radius: 10px;
  }
  
  
  .text-h4 {
    color: #ffffff; 
  }
  #ba{
    color: white;
  }

  img#oz {
    width: 800px;
}
  
  </style>
  
  
  
  
  
  
  