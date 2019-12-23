<template>
  <div>
    {{ checkbox }}
    <div
      v-for="(field, index) in [{ type: 'checkbox', value: 'TEST ' }]"
      :key="index"
    >
      <!-- <input type="checkbox" :value="field.value" v-model="checkbox" /> -->
      <!-- Works with type="checkbox" -->

      <input :type="field.type" :value="field.value" v-model="checkbox" />
      <!-- Doesn't work with dynamic binding :type="field.type" -->
      {{ field }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'InputExample',
  data: () => ({
    checkbox: []
  })
};
</script>
