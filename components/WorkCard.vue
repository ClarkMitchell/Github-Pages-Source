<template>
  <div class="card">
    <a :href="work.url">
      <div class="card-image">
        <figure class="image is-4by3">
          <img :src="work.image" :alt="work.imageAlt">
        </figure>
      </div>
      <div class="card-content">
        <div class="media-content">
          <div class="subtitle dark-text">
            {{ work.name }}
          </div>
        </div>
      </div>
    </a>
    <div class="content">
      {{ work.text }}
    </div>
    <footer class="card-footer">
      <a class="card-footer-item" :href="work.sourceUrl">
        <span>
          <figure class="centered-image">
            <img src="/GitHub-Logo.jpg" alt="Github icon">
          </figure>
          Source
        </span>
      </a>
    </footer>
  </div>
</template>

<script>
export default {
  props: ['work'],
};
</script>

<style scoped>
.dark-text.subtitle {
  color: hsl(0, 0%, 21%);
  text-align: center;
}

.content {
  margin: 1.5em;
}
</style>
