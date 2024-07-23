<template>
  <article class="video-container">
    <iframe src="https://www.youtube.com/embed/jXHLvTlTWLE?si=nghLE6tVS-aivk8m" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </article>
</template>
<script>
export default {
    name: 'VideoDisciplina',
    props: {
        msg: String
    }
};
</script>