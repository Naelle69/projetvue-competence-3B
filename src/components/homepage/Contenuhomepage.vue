<template>   
  <header>
    <div class="contenuhomepage">
      <div class="logohomepage mt-11 mb-8">
        <img src="@/assets/images/logobeige.svg" alt="Logo Pok'Gourmet" width="70"/>
      </div>

      <div class="pokgourmet w-70 ml-16 mb-4">
        <h1 class="mb-5">Pok'Gourmet</h1>
        <h2 class="h2marron mb-6">Donnez vie à vos envies</h2>
        <p class="pgourmet mb-6">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc, ut auctor lectus . At enim aucacilisis eget. Condimenpellentesque risus, tincidunt. Pro morbi tempor, curabitur neque quam convallis.</p>
        <button class="bouton1 mb-8" name="button" type="button"> Découvrir nos produits </button>
      </div>

      <div class="offredelasemaine w-72 ml-16">
        <iframe class="videohompepage" src="https://www.youtube.com/embed/ez4zQr6CSnY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <div class="offre">
            <h4 class="h4vert mb-4">Offre de la semaine</h4>
            <p class="ptexte mb-2">Pok'Veggie </p>
            <p class="ptexte mb-2">7€</p>
            <button class="bouton2" name="button" type="button"> Acheter </button>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
header{
  background-color: #62615C;
  width: 100%;
  height: 770px;
}

.contenuhomepage{
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  position: relative;
  top: 50px;
  
}

.offredelasemaine{
  background-color: #ffffff;
  border-radius:50px 5px 0px 0px;
  padding: 1rem;
  padding-bottom: 15%;
  position:relative;
  top: 25px;
}

.videohompepage{
  border-radius:50px 5px 50px 5px;
  box-shadow: 1px 1px 3px 3px rgba(222, 162, 105, 0.5); 
  width: 97%;
  height: auto;
  margin-bottom: 20px;
}

.offre{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

.pokgourmet{
  height: auto;
  width: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}



/* MOBILE */
@media screen and (min-width: 320px) and (max-width:480px){
  header{
  position: relative;
  top:-80vh;
  z-index: -1;
}

.pgourmet{
      display: none; 
    }
}

/* TABLETTE */
@media screen and (min-width:481px) and (max-width:768px){
  header{
    width: 100%;
    height: 810px;
    margin: 0%;
    padding: 0%;
  }

  .contenuhomepage{
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      height: 600px;
      margin-left: 0%;
      margin-right: 0%; 
    }
  
    .offredelasemaine{
      display: flex;
      flex-direction: row-reverse;      
      justify-content: space-evenly;
      align-items: center;
      width: 80%;
      height: 350px;
      border-radius: 0px 5px 50px 0px;
      position: relative;
      left: -120px;
      padding: 50px;
    }

    .offre{
      margin-left: 20px;
      margin-right: 20px;
    }

    .videohompepage{
      width: 50%;
      height: 100%;
    }
  
    .pokgourmet{
      width: 90%;
      height: 350px;
      display: flex;
      align-items:flex-start;
      margin-left: 0%;
      margin-top: 5%;
    }
}

/* ORDINATEUR */
@media screen and (min-width:768px) and (max-width:2570px){

  header{
      width: 100%;
      height: 100vh;
      margin: 0%;
      padding: 0%;
    }

    .contenuhomepage{
      display: flex;
      flex-direction: row-reverse;
      justify-content: space-evenly;
      width: 100%;
      height: 100%;
      margin-left: 0%;
      margin-right: 0%;
    }
  
    .offredelasemaine{
      display: flex;
      flex-direction: row-reverse;
      justify-content: center;
      align-items: center;
      width: 70%;
      height: 500px;
      padding: 0%;
      padding-right: 20px;
      position: relative;
      left: -100px;
      border-radius: 0px 5px 50px 0px;
      box-shadow: 1px 1px 3px 3px rgba(222, 162, 105, 0.3); 
    }
  
    .pokgourmet{
      width: 50%;
      height: 500px;
      margin-right: 150px;
      margin-left: 50px;
      justify-content: space-around;
      align-items: flex-start;
    }
  
    .videohompepage{
      height: 400px;
      width: 60%;
      margin-bottom: 0px;
      border-radius:30px 5px 30px 5px;  
    }
  
    .offre{
      margin-left: 70px;
      width: 30%;
    }
}
</style>
