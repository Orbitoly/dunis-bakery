<script setup>
const props = defineProps({
  modelValue: { type: Object, required: true },
});

const billing = toRef(props, 'modelValue');
</script>

<template>
  <div class="w-full grid gap-4 lg:grid-cols-2">
    <div class="w-full">
      <label for="first-name">{{ $t('messages.billing.firstName') }}</label>
      <input v-model="billing.firstName" placeholder="דניאלה" type="text" required />
    </div>

    <div class="w-full">
      <label for="last-name">{{ $t('messages.billing.lastName') }}</label>
      <input v-model="billing.lastName" placeholder="ששון" type="text" required />
    </div>

    <div class="w-full">
      <label for="email">{{ $t('messages.billing.email') }}</label>
      <input
        v-model="billing.email"
        placeholder="johndoe@email.com"
        type="email"
        pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$"
        required />
    </div>

    <div class="w-full">
      <label for="phone">{{ $t('messages.billing.phone') }}</label>
      <input v-model="billing.phone" placeholder="0524555251" type="tel" />
    </div>

    <div class="w-full col-span-full">
      <label for="address1">{{ $t('messages.billing.address1') }}</label>
      <input v-model="billing.address1" placeholder="רחוב המסיק" type="text" required />
    </div>

    <div class="w-full col-span-full">
      <label for="address2">{{ $t('messages.billing.address2') }}</label>
      <input v-model="billing.address2" placeholder="הגורן 3" type="text" />
    </div>

    <div class="w-full">
      <label for="city">{{ $t('messages.billing.city') }}</label>
      <input v-model="billing.city" placeholder="תל אביב" type="text" required />
    </div>

    <div class="w-full">
      <label for="country">{{ $t('messages.billing.country') }}</label>
      <CountrySelect v-model="billing.country" :default-value="billing.country" />
    </div>
  </div>
</template>
