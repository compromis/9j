<script setup>
defineProps({
  socials: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <ul class="socials list-reset">
    <li v-for="profile in socials" :key="profile.icon">
      <a :href="profile.url" target="_blank" :aria-label="profile.name">
        <Icon :name="profile.icon" />
      </a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
.socials {
  gap: var(--spacer-4);
  margin-top: var(--spacer-4);

  a {
    font-size: 1.5rem;
    color: var(--gray);
    opacity: .5;
    transition: .25s ease;

    &:hover {
      opacity: 1;
    }
  }
}
</style>