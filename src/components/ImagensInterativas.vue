<template>
  <article class="flex-container">
    <article class="img-container">
      <img class="cachorro-img" src="@/assets/cachorro1.jpg" alt="Cachorro 1">
    </article>
    <article class="img-group">
      <img class="cachorro-img" src="@/assets/cachorro2.jpg" alt="Cachorro 2">
      <img class="cachorro-img" src="@/assets/cachorro3.jpg" alt="Cachorro 3">
    </article>
  </article>
</template>
<script>
export default {
    name: 'ImagensInterativas',
    props: {
        msg: String
    }
};
</script>