<script setup>
const props = defineProps({
  title: String,
  body: String,
  href: String,
});

const { href, title, body } = props;
</script>

<template>
  <div class="bg-gray-600 text-white p-4 rounded-lg">
    <a :href="href" target="_blank">
      <h2>
        {{ title }}
        <span>&rarr;</span>
      </h2>
      <p>{{ body }}</p>
    </a>
  </div>
</template>
