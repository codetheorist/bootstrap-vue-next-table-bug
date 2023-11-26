<template>
  <div>
    <BCard>
      <BForm>
        <BFormGroup label="Search" label-cols="3" label-for="search-input">
          <BFormInput v-model="search" id="search-input" />
        </BFormGroup>
      </BForm>
      <BTable :filter="search" :provider="provider" show-empty />
    </BCard>
  </div>
</template>
<script setup>
import { ref } from 'vue';
const search = ref('');
const provider = (options) => {
  console.log(options);

  return [];
};
</script>
