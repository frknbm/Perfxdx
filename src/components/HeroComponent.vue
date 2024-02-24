<template>
    <div class="video-section">
    <v-container class="pt-15">
        <v-row>
        
            <v-col lg="6">
                <br><br>
                <h4 class="intro-text">YENİ NESİL PERFORMANS YÖNETİM <br>UYGULAMASI</h4>
                <p class="description"><a>SabancıDx</a> tarafından geliştirilen, yeni nesil<br> performans yönetim uygulaması Perfx, 
                    ileri ve <br>geri bildirim sistemi ile çalışan hedeflerinizi<br> şirket hedeflerinizle uyumlu hale getirmenizi <br>sağlar.</p>
                <a href="https://www.hrwedx.com/" target="_blank">
                <v-btn  color="white" class="white -- text" rounded><v-icon>mdi-play-circle</v-icon>İZLE</v-btn></a>

                
        

            </v-col>
            <c-col lg="6">
               
            </c-col>
            <v-col lg="6">
                <a href="https://www.hrwedx.com/" target="_blank">
                <img style="float: right; " width="100%" src="./../assets/perfx-video.png" alt=""></a>


            </v-col>
        </v-row>


    </v-container>
</div>

</template>



<script>
      export default {
        name:"HeroComponent"
      }
</script>


<style scoped>
h4.intro-text {
    font-size: 33px;
    font-weight: bold;
    font-family: system-ui;
    color: hwb(0 100% 0%);
}
p.description{
    font-size: 25px;
    font-weight: bold;
    font-family: system-ui;
    color: #ffffff;
}
.container.pt-15 {
    background-color: #344199;
}
.video-section {
    background-color: #344199;
}



</style>