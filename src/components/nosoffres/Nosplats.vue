<template>
        <div class="nosplats">
            <div class="h offres ml-4 mt-10">
                <h2 class="h2marron mb-4"> Nos offres </h2>
                <h3 class="h3vert mb-4"> Nos plats </h3>
            </div>

         
            <Sectionplats v-for="(plat,index) in plats" :key="index" :id="plat.id" :soustitre="plat.soustitre" :texte="plat.texte" :image="plat.image" :button="plat.boutton" />
            <!-- <div class="relative overflow-auto mt-16">
                <div class="plat p-12 w-2/3 h-full shrink-0 ">
                    <span class="sm:w-40">
                        <h4 class="h4vert mb-4"> Pok au saumon fumé</h4>
                        <p class="ptexteplat pr-12">
                            Lorem ipsum dolor sit amet. Pellentesque habitant morbi tristique senectus 
                            neque. Mauris gravida odio.
                        </p>
                    </span>
                    <img class="imageplat w-32 rounded-full" src="@/assets/images/plat-poke-bowl2.jpg" alt="Plat saumon"/>
                </div> -->

                <!-- <div class="plat shrink-0 ">
                    <span>
                        <h4 class="h4vert mb-4"> Pok au saumon fumé</h4>
                        <p class="ptexteplat">
                            Lorem ipsum dolor sit amet. Pellentesque habitant morbi tristique senectus 
                            neque. Mauris gravida odio.
                        </p>
                    </span> 
                    <img src="@/assets/images/plat-poke-bowl.jpg" alt="Plat saumon" width="120"/>
                </div>
                <div class="plat shrink-0 ">
                    <span>
                        <h4 class="h4vert mb-4"> Pok au saumon fumé</h4>
                        <p class="ptexteplat">
                            Lorem ipsum dolor sit amet. Pellentesque habitant morbi tristique senectus 
                            neque. Mauris gravida odio.
                        </p>
                    </span> 
                    <img src="@/assets/images/plat-poke-bowl2.jpg" alt="Plat saumon" width="120"/>
                </div>
                <div class="plat shrink-0 ">
                    <span>
                        <h4 class="h4vert mb-4"> Pok au saumon fumé</h4>
                        <p class="ptexteplat">
                            Lorem ipsum dolor sit amet. Pellentesque habitant morbi tristique senectus 
                            neque. Mauris gravida odio.
                        </p>
                    </span> 
                    <img src="@/assets/images/plat-poke-bowl.jpg" alt="Plat saumon" width="120"/>
                </div> -->
            <!-- </div> -->
        </div>

</template>

<script>
// @ is an alias to /src
import Sectionplats from '@/components/nosoffres/Sectionplats.vue'
import axios from 'axios'

export default {
  name: 'Nosplats',
  components: {
    Sectionplats,
  },

  data(){
        return {
            sectionplats:[],
            errors: [],
        }
  },
 
  // Fetches Details when the component is created.
  created() {
    axios.get('http://localhost:8080/plats.json')
    .then(response => {
      // JSON responses are automatically parsed.
      this.plats = response.data.plats
    })
    .catch(e => {
      this.errors.push(e)
    })
  }
}
</script>


<style scoped>
.relative {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: row;
}

.nosplats{
    overflow-x:auto;
  }
  
.plat{
  background-image: url("../../assets/images/fondblanc.svg");
  background-repeat: no-repeat;
}

 .plat img{
  position: relative;
  top: -170px;
  left: 150px;
  z-index: 1;
  box-shadow: 2px 2px 3px 3px rgb(215, 157, 102, 0.4);
}


/* TABLETTE */
@media screen and (min-width:481px) and (max-width:768px){

.nosplats{
    margin-top: 50px;
    margin-left: 50px;
    margin-right: 50px;
}
 
.plat{
    width: 264px;
    padding-top: 60px;
    margin-right: 0%;
    margin-left: 0%;
}

.plat img{
    width: 148px;
    border-radius: 50%;
    position: relative;
    top: -170px;
    left: 150px;
    z-index: 1;
}

.ptexteplat{
    width: 200px;
}

}


/* LAPTOP ET DESKTOP */
@media screen and (min-width:769px) and (max-width:2570px){

    .nosplats{
    margin-top: 150px;
    margin-left: 85px;
    }
 
    .plat{
    width: 344px;
    padding: 70px;
    }

    .imageplat{
    width: 200px;
    border-radius: 50%;
    position: relative;
    top: -180px;
    left: 180px;
    z-index: 1;
    }
}

</style>