<template>
      <div class="relative overflow-auto mt-16">
                <div class="plat p-12 w-2/3 h-full shrink-0 ">
                    <span class="sm:w-40">
                        <h4 class="h4vert mb-4"> {{soustitre}}</h4>
                        <p class="ptexteplat pr-12">{{texte}}</p>
                    </span>
                    <img class="imageplat w-32 rounded-full" :src='`${image}`' alt="Plat saumon"/>
                    <button> {{button}} </button>
                </div>
      </div>
</template>

<script>
export default {
  name: 'Sectionplats',
  props: {
    id: Number,
    soustitre:String,
    texte:String,
    image:String,
    button:String,
  }
}
</script>