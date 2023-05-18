<template>
  <select :value="defaultValue" @change="select">
    <option v-for="country in countries" :key="country.countryName" def :value="country.countryCode" :checked="country.countryCode === defaultValue">
      {{ country.countryName }}
    </option>
  </select>
</template>

<script>
export default {
  props: {
    defaultValue: {
      type: String,
      default: 'IE',
    },
  },
  data() {
    return {
      countries: [
       
        { countryName: 'ישראל', countryCode: 'IL' },
       
      ],
    };
  },
  methods: {
    select(evt) {
      this.$emit('input', evt.target.value);
    },
  },
};
</script>

<style scoped lang="postcss">
select {
  height: 42px;
}
</style>
