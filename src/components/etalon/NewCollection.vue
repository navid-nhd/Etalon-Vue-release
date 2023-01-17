<template>
    <section id="new-collection">
      <main class="container mx-auto">
          <h2 class="section-title py-8">
              New Collection
          </h2>
          <div class="flex flex-wrap lg:flex-nowrap lg:gap-6">
              <div class="w-full lg:w-5/12">
                  <div class="left-showcase relative w-full rounded-3xl mb-8">
                      <h3 class="left-showcase-title font-bold">
                          Men’s Jacket Collection
                      </h3>
                      <div class="left-showcase-picture-holder">
                          <img class="left-showcase-picture block absolute bottom-0 left-1/2" src="src/image/2.png" alt="Jacket" >
                      </div>
                      <div class="left-showcase-btn absolute cursor-pointer">
                          <route-link to="/" class="btn inline-block text-white bg-zinc-900 hover:bg-zinc-700">Discover Now</route-link>
                      </div>
                  </div>
              </div>
              <div class="w-full lg:w-7/12">
                  <div class="right-showcase w-full bg-amber-300 rounded-3xl mb-8 flex flex-col items-end text-center relative">
                      <h3 class="right-showcase-title font-bold">
                          Men’s Glasses<br> Collection
                      </h3>
                      <div class="right-showcase-off font-bold text-center capitalize">
                          40% OFF
                      </div>
                      <div class="right-showcase-picture-holder">
                          <img class="right-showcase-picture block absolute bottom-0" src="src/image/3.png" alt="Glasses" >
                      </div>
                      <div class="right-showcase-btn absolute cursor-pointer">
                          <router-link to="/" class="btn text-white inline-block bg-zinc-900 hover:bg-zinc-700 hover:text-white" title="Discover" >Discover Now</router-link>
                      </div>
                  </div>
              </div>
          </div>
      </main>
  </section>
</template>
<script>

</script>
<style scoped>
.section-title {
    font-size: 32px;
    line-height: 32px;
}
/* ------- NEW COLLECTION ------*/

.left-showcase {
    height: 410px;
    background-color: #c5c2ca;
}
.left-showcase-title,
.right-showcase-title {
    font-size: 18px;
    line-height: 18px;
    padding: 18px;
}
.left-showcase-picture {
    width: 197px;
    height: 340px;
    transform: translateX(-50%) scaleX(-1);
}
.left-showcase-btn,
.right-showcase-btn {
    right: 18px;
    bottom: 18px;
    ;
}
.right-showcase {
    height: 245px;
}
.right-showcase-title {
    width: 175px;
    padding-bottom: 52.47px;
    margin: 0;
}
.right-showcase-off {
    font-family: var(--etalon-font-secondry);
    font-size: 24px;
    line-height: 28px;
    padding:0 40px 41.8px 0;
}
.right-showcase-picture {
    width: 169px;
    height: 216px;
    left: 20px;
}

@media  screen and (min-width : 992px) {
    .section-title {
        font-size: 48px;
        line-height: 48px;
        padding: 70px 0;
    }
    .left-showcase {
        height: 550px;
        margin-bottom: 70px;
    }
    .left-showcase-title,
    .right-showcase-title {
        font-size: 24px;
        line-height: 40px;
        padding: 24px;
    }
    .left-showcase-btn {
        right: 24px;
        bottom: 24px;
    }
    .left-showcase-picture {
        width: 278px;
        height: 478px;
    }
    .right-showcase {
        width: 100%;
        height: 550px;
        margin-bottom: 70px;
    }
    .right-showcase-title {
        padding: 71px 98px 95px 0;
        width: 283px;
    }
    .right-showcase-off {
        font-size: 48px;
        line-height: 56px;
        padding-right: 96px;
    }
    
    .right-showcase-picture {
        width: 230px;
        height: 430px;
        left: 20px;
    }
}
@media  screen and (min-width : 1200px) {
    .right-showcase-picture {
        display: block;
        width: 375px;
        height: 520px;
        left: 40px;
    }
}
</style>