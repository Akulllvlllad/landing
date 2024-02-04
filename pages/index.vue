<template>
  <section>
    <n-carousel :space-between="20" draggable>
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel1.jpeg"
      >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg"
      >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel3.jpeg"
      >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel4.jpeg"
      >
    </n-carousel>
  </section>


  <section>
    <header>
      <NH2>Популярные товары</NH2>
    </header>

    <ul class="list-popular">
      <li v-for="i of 6" :key="i">
        <article class="card-popular"> 
            <div class="card-popular__image">
              <NImage
                class="NImage"
                object-fit="cover"
                :show-toolbar="false"
                :lazy="true"
                width="100%"
                :src="`/static/msg1271329192-13336${i}.jpg`"
              />
            </div>

            <div>
              <h5> товар {{ i }}</h5>
              <p> цена {{ i * 1000 }} р</p>
            </div>
        </article>
      </li>
    </ul>
  


  </section>
 
</template>
<style scoped lang="scss">
.carousel-img {
  width: 100%;
  height: 240px;
  object-fit: cover;
}

.list-popular{
  display: grid;
  grid-template-columns: repeat(2,1fr);
  gap: 32px 8px;
  padding: 0 24px;
  list-style: none;
}


.card-popular{
  
  &__image{
    overflow: hidden;
    border-radius: 10px;
    aspect-ratio: 1 / 1;
    .NImage{
      height: 100%;
    }
  }
}
</style>