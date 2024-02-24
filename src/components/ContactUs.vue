<template>
    <v-container class="my-15">
      <v-row justify="center">
        <v-col lg="12" class="text-center">
          <br /><br /><br /><br /><br /><br />
          <v-subheader class="text-h4 justify-center">İLETİŞİM</v-subheader>
        </v-col>
        <v-col lg="6">
          <v-subheader class="text-h4 justify-center">SabancıDx Dijital Kampüs</v-subheader>
          <v-subheader class="text-h9 justify-center">
            Küçük Çamlıca Mahallesi, Kısıklı Caddesi, No. 56,<br />
            PK 34696 Üsküdar / İSTANBUL
          </v-subheader>
          <br />
          <v-subheader class="text-h4 justify-center">İletişim Merkezi</v-subheader>
          <v-subheader class="text-h9 justify-center">(+90) 850 228 08 08</v-subheader>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12040.535728258335!2d29.0510327!3d41.0223257!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14cacbb6a65c3f65%3A0x82030061eb8afdbb!2sSabanc%C4%B1Dx!5e0!3m2!1str!2str!4v1689315114476!5m2!1str!2str"
            width="500"
            height="450"
            style="border: 0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </v-col>
        <v-col lg="6">
          <v-form ref="form">
            <v-select
              v-model="select"
              :rules="[v => !!v || 'Doldurulması Gerekiyor']"
              label="Size Nasıl Yardımcı Olabiliriz?"
              :items="['Size Nasıl Yardımcı Olabiliriz?','Pefx hakkında bilgi almak istiyorum','Entegre çözümü','diğer']"
              required
            ></v-select>
            <v-text-field v-model="name" :counter="60" :rules="nameRules" label="adınız" required></v-text-field>
            <v-text-field v-model="surname" :counter="60" :rules="nameRules" label="soyadınız" required></v-text-field>
            <v-text-field v-model="email" :counter="60" :rules="emailRules" label="e-posta" required></v-text-field>
            <v-text-field v-model="phoneNumber" :counter="60" :rules="numberRules" label="telefon numaranız" required></v-text-field>
            <v-text-field v-model="companyName" :counter="60" :rules="nameRules" label="Firma ismi" required></v-text-field>
            <v-text-field v-model="message" :counter="100" :rules="nameRules" label="Mesajınız" required></v-text-field>
            <v-checkbox
              v-model="checkbox"
              label="Kişisel verilerimin sunucusu yurtdışında bulunan bulut sistemlerin kullanılması sebebiyle yurt dışına aktarılmasını onaylıyorum."
              required
            ></v-checkbox>
            <v-card class="mb-12" color="surface-variant" variant="tonal">
              <v-card-text class="text-medium-emphasis text-caption">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et eaque hic sint incidunt commodi omnis dolores.
                Labore sed provident dolore officiis et consectetur vel odit accusantium, possimus qui quas iure!
              </v-card-text>
            </v-card>
            <v-btn
              color="#344199"
              :disabled="loading"
              :loading="loading"
              block
              class="text-none mb-4"
              size="x-large"
              variant="flat"
              @click="loading = !loading; submitForm()"
              id="ar"
            >
              GÖNDER
            </v-btn>
          </v-form>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'ContactUs',
    data: () => ({
      loading: false,
      select: '',
      name: '',
      surname: '',
      email: '',
      phoneNumber: '',
      companyName: '',
      message: '',
      checkbox: false,
    }),
    computed: {
      nameRules() {
        return [v => !!v || 'Doldurulması Gerekiyor'];
      },
      emailRules() {
        return [
          v => !!v || 'Doldurulması Gerekiyor',
          v => /.+@.+\..+/.test(v) || 'Geçerli bir e-posta adresi girin',
        ];
      },
      numberRules() {
        return [v => !!v || 'Doldurulması Gerekiyor', v => /^\d+$/.test(v) || 'Sadece rakam girişi yapın'];
      },
    },
    methods: {
      submitForm() {
        if (this.$refs.form.validate()) {
          
          alert('Mesajınız gönderilmiştir en kısa sürede döneceğiz.');
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .theme--light.v-subheader {
    color: #1f1f1f;
  }
  #ar{
    color: white;
  }
  </style>
  