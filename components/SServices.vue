<template>
  <div class="c-services">
    <div
      class="c-service"
      :class="`enter-fade-up enter-delay-${index + 2}`"
      v-for="(service, index) in services"
    >
      <div class="c-service__icon">
        <img
          class="c-service__image"
          :src="service.image.data.url"
          :alt="service.title"
        />
      </div>
      <div class="c-service__description">
        <h2>{{ service.title }}</h2>
        <div v-html="service.description" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'SServices',
  props: {
    services: Array
  }
}
</script>
