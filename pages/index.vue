<template>
  <div>
    <h1>this is scss projecct</h1>
    <home-viwe></home-viwe>
    <div class="">
      <ssr-carousel show-dots>
        <slide v-for="i, ind in imgArray" :key="ind">
        <img :src="i.img" alt="">
        </slide>
      </ssr-carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      imgArray: [
        { img: 'https://www.imgacademy.com/themes/custom/imgacademy/images/helpbox-contact.jpg' },
        { img: 'https://www.imgacademy.com/themes/custom/imgacademy/images/helpbox-contact.jpg' },
        { img: 'https://www.imgacademy.com/themes/custom/imgacademy/images/helpbox-contact.jpg' },
      ]
    }
  },
}
</script>
