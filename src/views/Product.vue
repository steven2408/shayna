<template>
  <div class="product">
    <HeaderShayna />
    <div class="breacrumb-section">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="breadcrumb-text product-more text-left">
              <router-link to="/"> <i class="fa fa-home"></i> Home </router-link>
              <span>Detail</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img class="product-big-img" :src="gambar_default" alt="" />
                </div>
                <div class="product-thumbs">
                  <carousel class="product-thumbs-track ps-slider" :dots="false" :nav="false">
                    <div class="pt" @click="changeImage(thumbs[0])" :class="thumbs[0] == gambar_default ? 'active' : '' ">
                      <img src="img/products/shoes-1.PNG" alt="" />
                    </div>

                    <div class="pt" @click="changeImage(thumbs[1])" :class="thumbs[1] == gambar_default ? 'active' : '' ">
                      <img src="img/products/shoes-2.PNG" alt="" />
                    </div>

                    <div class="pt" @click="changeImage(thumbs[2])" :class="thumbs[2] == gambar_default ? 'active' : '' ">
                      <img src="img/products/shoes-3.PNG" alt="" />
                    </div>

                    <div class="pt" @click="changeImage(thumbs[3])" :class="thumbs[3] == gambar_default ? 'active' : '' ">
                      <img src="img/products/shoes-4.PNG" alt="" />
                    </div>

                  </carousel>
                </div>
              </div>
              <div class="col-lg-6 text-left">
                <div class="product-details">
                  <div class="pd-title">
                    <span>oranges</span>
                    <h3>Pure Pineapple</h3>
                  </div>
                  <div class="pd-desc">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam
                      laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id
                      accusantium! Autem.
                    </p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi,
                      nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate
                      voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                      Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus
                      voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam
                      quia sit nihil dolores.
                      Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id
                      dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore
                      obcaecati, unde quam
                      impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                    </p>
                    <h4>$495.00</h4>
                  </div>
                  <div class="quantity">
                    <router-link to="/cart"><a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a></router-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <relatedShayna />
    <footerShayna />
  </div>
</template>

<script>
  import HeaderShayna from '@/components/headerShayna.vue';
  import footerShayna from '@/components/footerShayna';
  import carousel from 'vue-owl-carousel';
  import relatedShayna from '@/components/relatedShayna';

  export default {
    name: "product",
    components: {
      HeaderShayna,
      footerShayna,
      carousel,
      relatedShayna
    },
    data() {
      return{
        gambar_default: "img/products/shoes-1.PNG",
        thumbs: [
          "img/products/shoes-1.PNG",
          "img/products/shoes-2.PNG",
          "img/products/shoes-3.PNG",
          "img/products/shoes-4.PNG"
        ]
      }
    },
    methods: {
      changeImage(urlImage){
        this.gambar_default = urlImage;
      }
    }
  }
</script>

<style scoped>
.product-thumbs .pt{
  margin-right: 15px;
}
</style>