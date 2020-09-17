<template>
  <div class="movies">
    <div class="jumbotron" v-for="movie in movies" :key="movie.title">
      <div class="row">
        <img :src="movie.imgUrl" class="col-12 col-md-6">
        <div class="col-12 col-md-6">
          <h4 class="display-4">{{ movie.title }}</h4>
          <hr class="my-4">
          <span class="badge p-2" :class="[movie.metadata.type]">{{movie.metadata.typeLabel}}</span> 
          <hr class="my-4">
          <p class="lead text-justify">{{ movie.description }}</p>
          <hr class="my-4">
          <p class="lead">
            <a class="btn btn-primary btn-lg" href="#" role="button">REGARDER EN STREAMING</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Movies',
  data() {
    return {
      movies: [
        {
          imgUrl: "https://www.telerama.fr/sites/tr_master/files/styles/simplecrop1000/public/003946.jpg-r_1920_1080-f_jpg-q_x-xxyxx_0.jpg?itok=Z_rQDxr7",
          title: "Dernier train pour Busan",
          description: "Seok-woo, jeune homme d'affaires débordé, accepte de ramener sa fille Soo-an chez sa mère, dont il est séparé, à Busan. Ils embarquent dans un train, sans se douter que la ville qu'ils s'apprêtent à quitter vient d'être contaminée par un dangereux virus transformant la population en mort vivants. Le train finit par quitter la gare mais une femme contaminée est parvenue à grimper à bord. Elle menace à présent l'ensemble des voyageurs.",
          metadata: {
            type: "badge-warning",
            typeLabel: "Horror"
          }
        },
        {
          imgUrl: "https://fr.web.img3.acsta.net/newsv7/19/11/27/14/23/4073575.jpg",
          title: "Le Tombeau des Lucioles",
          description: "Japon, été 1945. Après le bombardement de Kobé, Seita, un adolescent de quatorze ans et sa petite soeur de quatre ans, Setsuko, orphelins, vont s'installer chez leur tante à quelques dizaines de kilomètres de chez eux. Celle-ci leur fait comprendre qu'ils sont une gêne pour la famille et doivent mériter leur riz quotidien. Seita décide de partir avec sa petite soeur. Ils se réfugient dans un bunker désaffecté en pleine campagne et vivent des jours heureux illuminés par la présence de milliers de lucioles. Mais bientôt la nourriture commence cruellement à manquer.",
          metadata: {
            type: "badge-secondary",
            typeLabel: "Sad"
          }
        },
        {
          imgUrl: "https://thumb.canalplus.pro/http/unsafe/1280x720/filters:quality(80)/img-hapi.canalplus.pro/ServiceImage/ImageID/83548883",
          title: "Wall-E",
          description: "Wall E, un petit robot, est le dernier être sur Terre ! 700 ans plus tôt, l'humanité a déserté notre planète en lui laissant le soin de nettoyer la Terre. Mais Wall E a développé un petit défaut technique : une forte personnalité ! Curieux et indiscret, il est surtout très seul. Sa vie va être bouleversée avec l'arrivée d'Eve, une petite robote. Wall E va tout mettre en uvre pour la séduire.",
          metadata: {
            type: "badge-danger",
            typeLabel: "Cute"
          }
        },
        {
          imgUrl: "https://www.weculte.com/wp-content/uploads/2020/05/russel-crowe-gladiator-696x463.jpg",
          title: "Gladiator",
          description: "Le général romain Maximus est le plus fidèle soutien de l'empereur Marc Aurèle, qu'il a conduit de victoire en victoire. Jaloux du prestige de Maximus, et plus encore de l'amour que lui voue l'empereur, le fils de Marc Aurèle, Commode, s'arroge brutalement le pouvoir, puis ordonne l'arrestation du général et son exécution. Maximus échappe à ses assassins, mais ne peut empêcher le massacre de sa famille. Capturé par un marchand d'esclaves, il devient gladiateur et prépare sa vengeance.",
          metadata: {
            type: "badge-danger",
            typeLabel: "Sad"
          }
        },
        {
          imgUrl: "https://www.ecranlarge.com/uploads/image/001/087/joker-photo-1087850.jpg",
          title: "Joker",
          description: "Dans les années 1980, à Gotham City, Arthur Fleck, un comédien de stand-up raté est agressé alors qu'il ère dans les rues de la ville déguisé en clown. Méprisé de tous et bafoué, il bascule peu à peu dans la folie pour devenir le Joker, un dangereux tueur psychotique.",
          metadata: {
            type: "badge-success",
            typeLabel: "Wesh"
          }
        },
        {
          imgUrl: "https://aws1.vdkimg.com/film/1/3/3/5/1335955_backdrop_scale_1280xauto.jpg",
          title: "Cinquante nuances de black",
          description: "Dans cette parodie, le comique, Marlon Wayans, met la fessée à Cinquante nuances de Grey. Wayans incarne le séduisant Christian Black qui va tomber sous le charme de l'innocence Hannah jusqu'à lui proposer un pacte d'amour placé sous le signe du S.M. S.M. comme Super Marrant.",
          metadata: {
            type: "badge-primary",
            typeLabel: "Oui"
          }
        },
      ]
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
