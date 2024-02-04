<template>
    <div class="text-bg-dark me-md-3 pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden">
      <div class="my-3 py-3">
        <h2 class="display-5">{{title}}</h2>
        <p class="lead">{{price}}</p>
        <router-link :to="'/product/' + keyy" class = "display-7">Accéder au produit</router-link>
      </div>
      <div class="bg-body-tertiary shadow-sm mx-auto" style="width: 100%; border-radius: 21px 21px 0 0;">
        <div :id="'carouselExampleSlidesOnly_' + keyy" class='carousel slide' data-bs-ride='carousel' data-bs-interval='2000'>
            <div class='carousel-inner'>
                <div v-for='(image, index) in pictures' :class="{'carousel-item': true, 'active': index === 0}">
                    <img class='d-block w-100 mx-auto' :src="'../assets/productImages/' + idimages + '/' + image">
                </div>
            </div>
            <button class='carousel-control-prev' type='button' :data-bs-target="'#carouselExampleSlidesOnly_' + keyy"  data-bs-slide='prev'><span class='carousel-control-prev-icon' aria-hidden='true'></span><span class='visually-hidden'>Previous</span></button>
            <button class='carousel-control-next' type='button' :data-bs-target="'#carouselExampleSlidesOnly_' + keyy"  data-bs-slide='next'><span class='carousel-control-next-icon' aria-hidden='true'></span><span class='visually-hidden'>Next</span></button>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'ProductComponent',
  props: ['title', 'description', 'price', 'idimages','pictures', 'typee', 'sendable']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
