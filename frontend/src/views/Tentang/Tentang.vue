<template>
    <div >
             <Navbar isBrand/>
       
        <Header :style="'background-color: rgba(0, 0, 0, 0.03);'" :title="$t('about.title')"/>
        <section class="section-merdeka">
          <div class="container-fluid">
            <b-row >
                <b-col lg="4" xl="3" class="d-flex justify-content-center align-items-center pt-4">
                    <b-img class="logo-about"  src="assets/img/Logo-2x.png"></b-img>
                </b-col>
                <b-col lg="8" xl="9">
                  <div class="container-fluid text-content">
                    <p class="mt-5"><strong style="font-weight:bold;">Merdeka!!</strong></p>
                    <p v-html="$t('about.aboutMerdekaFirstParagraph')">
                    
                     </p>
                     <p>
                      {{ $t("about.aboutMerdekaSecondParagraph") }}
                      <br/><br/>
                      {{ $t("about.aboutMerdekaThirdParagraph") }}
                      <router-link  class=" text-decoration-none" to="/pendaftaran">
                        <strong class="underline" style="color:#CB2B2B;">                      
                          {{ $t("about.aboutMerdekaJoinNow") }}
                        </strong>
                      </router-link>
                    </p>
                </div>
              </b-col>
            </b-row>
          </div>
        </section>
        <div class="about-kenapa-section  container-fluid ">
              <div class="wrapper">
                <b-row>
                    <b-col lg="3"  class="kenapa-wrapper pt-4">
                        <div >
                            <p class="title mt-3">
                            {{ $t("why") }}
                              <br/>
                              Merdeka Pulsa?
                            </p>
                            <div class="line-red"></div>
                        </div>
                    </b-col>

                    <b-col v-for="content in ContentList" v-bind:key="content.id" lg="3" md="6" sm="12"> 
                        <CardAbout
                        :gambar="content.gambar"
                        :title="content.title"
                        :caption="content.caption"
                        />
                    </b-col>

                </b-row>
              </div>
              <b-img class="stgh-lingkaran" src="assets/img/abouts/lingkaran.png"></b-img>
        </div>
      
    </div>
</template>
<script>

import {Header,Navbar,CardAbout} from '../../components';

export default {
    name:"Tentang",
    components:{
       CardAbout,
        Navbar,
        Header
    },
    data:()=>{
      return{
        ContentList:[
          {
            id:1,
            gambar:'monas.png',
            title: "about.whyMerdekaPulsa.place.title",
            caption:"about.whyMerdekaPulsa.place.content"
          },
          {
            id:2,
            gambar:'gedung.png',
            title: "about.whyMerdekaPulsa.trustWorthyCompany.title",
            caption:"about.whyMerdekaPulsa.trustWorthyCompany.content"
          },
          {
            id:3,
            gambar:'bank.png',
            title: "about.whyMerdekaPulsa.depositCompany.title",
            caption:"about.whyMerdekaPulsa.depositCompany.content"
          },
          {
            id:4,
           gambar:'shake-hand.png',
            title: "about.whyMerdekaPulsa.freeRegistration.title",
            caption:"about.whyMerdekaPulsa.freeRegistration.content"
          },{
            id:5,
            gambar:'terima-uang.png',
            title: "about.whyMerdekaPulsa.optionalBanks.title",
            caption:"about.whyMerdekaPulsa.optionalBanks.content"
          },{
            id:6,
            gambar:'koin.png',
            title: "about.whyMerdekaPulsa.smallDeposit.title",
            caption:"about.whyMerdekaPulsa.smallDeposit.content"
          },{
            id:7,
            gambar:'customer-service.png',
            title: "about.whyMerdekaPulsa.depositTime.title",
            caption:"about.whyMerdekaPulsa.depositTime.content"
          },{
            id:8,
            gambar:'uang.png',
            title: "about.whyMerdekaPulsa.competitivePrice.title",
            caption:"about.whyMerdekaPulsa.competitivePrice.content"
          },{
            id:9,
            gambar:'jam.png',
            title: "about.whyMerdekaPulsa.everytimeTransaction.title",
            caption:"about.whyMerdekaPulsa.everytimeTransaction.content"
          },
          {
            id:10,
            gambar:'dokument.png',
            title: "about.whyMerdekaPulsa.completeDocumentation.title",
            caption:"about.whyMerdekaPulsa.completeDocumentation.content"
          },{
            id:11,
            gambar:'dashboard.png',
            title: "about.whyMerdekaPulsa.easyMonitoring.title",
            caption:"about.whyMerdekaPulsa.easyMonitoring.content"
          }
        ]
      }
    }
}
</script>


<style lang="scss" scoped>
@import "@/views/Tentang/Tentang.scss";
</style>
