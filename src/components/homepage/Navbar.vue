<template>
    <div class="navbar"> 
      <div class="contentmobile">
        <div class="rechercher" href="lien">
          <img src="@/assets/images/svg-icones/loupemarron.svg" alt="Rechercher" width="20"/>
        </div>
        <div class="home" href="lien">
          <img src="@/assets/images/svg-icones/home.svg" alt="Rechercher" width="20"/>
        </div>
        <div class="contactnavigation">
          <div class="telephone" href="lien">
            <img src="@/assets/images/svg-icones/telephonemarron.svg" alt="Panier" width="19"/> 
          </div>
          <div class="enveloppe" href="lien">
            <img src="@/assets/images/svg-icones/enveloppe.svg" alt="Mon compte" width="20"/>
          </div>
          <div class="facebook" href="lien">
            <img src="@/assets/images/svg-icones/facebookmarron.svg" alt="Panier" width="19"/> 
          </div>
          <div class="instagram" href="lien">
            <img src="@/assets/images/svg-icones/instagrammarron.svg" alt="Mon compte" width="20"/>
          </div>
        </div>
        <div class="client">
          <div class="panier" href="lien">
            <img src="@/assets/images/svg-icones/paniermarron.svg" alt="Panier" width="19"/> 
          </div>
          <div class="moncompte" href="lien">
            <img src="@/assets/images/svg-icones/moncompte.svg" alt="Mon compte" width="20"/>
          </div>
        </div>
      </div>
    </div>

    <nav class="navbarweb z-10">
      <a class="navbarlogo" href="#">
        <img src="@/assets/images/logobeige.svg" width="90" alt="POK'GOURMET Logo"/>
      </a>

      <ul class="menunav justify-content-space-between" width="400">
        <li class="menunav-item">
          <a class="h5menu" href="#">Notre concept</a>
        </li>
        <li class="menunav-item">
          <a class="h5menu" href="#">Nos offres</a>
        </li>
        <li class="menunav-item">
          <a class="h5menu disabled">Idées recettes</a>
        </li>
        <li class="menunav-item">
          <a class="h5menu disabled">Blog conseils</a>
        </li>
      </ul>

      <div class="client">
        <!-- Icon -->
        <a class="panier" href="#">
          <img src="@/assets/images/svg-icones/paniermarron.svg" height="30" alt="POK'GOURMET Logo"/>
        </a>
        <a class="moncompte">
          <img src="@/assets/images/svg-icones/moncompte.svg" height="30" alt="POK'GOURMET Logo"/>
        </a>
      </div>
    </nav>
</template>

<style scoped>
.navbar{
  padding:80px 5px 80px 5px;
  height:80vh;
  width: 40px;
  background-color: #484526;
  border-radius: 15px 5px 15px 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  left: 20px;
  top: 70px;
} 

.navbar:hover{
  box-shadow: 1px 1px 3px 3px rgb(222, 162, 105, 0.2);
}

.contentmobile {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: column;
  height: 450px;
  }

.client{
  height: 80px;
  display: flex;
  justify-content: space-around;
  flex-direction: column;
}

.contactnavigation{
  height: 160px;
  display: flex;
  justify-content: space-around;
  flex-direction: column;
}

.navbarweb{
   display:none;
}
  


/* LAPTOP ET DESKTOP */
@media screen and (min-width:769px) and (max-width:2570px){
  .navbar{
    display:none
  }

  .navbarweb{
    position: fixed;
    top: 10px;
  }

  .navbarweb{
    height: 100px;
    width: 90%;
    background-color: #484526;
    border-radius:30px 5px 30px 5px;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    margin-top: 50px;
    margin-left: 100px;
    margin-right: 100px;
  }

  .navbarweb:hover{
    box-shadow: 1px 1px 3px 3px rgb(222, 162, 105, 0.2);
  }
  
  .menunav{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 500px;
  }

  .client{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 100px;
  }

  .contentweb{
    padding:  30px 60px 30px 60px;
    height: auto;
    width: 90%;
    border-radius:30px 5px 30px 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 100px;
  }
}

/* TABLETTE */
@media screen and (min-width:481px) and (max-width:768px){
    .navbar{
      display:none
    }
  
    .navbarweb{
      height: 80px;
      width: 90%;
      background-color: #484526;
      border-radius:30px 5px 30px 5px;
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
      margin-left: 5%;
      margin-right: 5%;
      position: fixed;
      top: 20px;
    }
  
    .navbarweb:hover{
      box-shadow: 1px 1px 3px 3px rgb(222, 162, 105, 0.2);
    }
    
    .navbarlogo{
      width: 60px;
    }

    .menunav{
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      width: 450px;
    }
  
    .client{
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      width: 60px;
    }
}

/* * MOBILE * */
@media screen and (min-width: 320px) and (max-width:480px){
  .navbarweb{
    display:none;
  }
}
</style>