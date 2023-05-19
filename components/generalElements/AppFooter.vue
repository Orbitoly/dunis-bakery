<script setup>
const runtimeConfig = useRuntimeConfig();
</script>

<template>
  <div class="bg-white" dir="rtl">
    <div class="container flex flex-wrap my-24 gap-12 justify-between md:gap-24">
      <div class="mr-auto">
        <Logo />
        <p dir="rtl" class="mt-4 text-sm text-gray-700 xl:max-w-sm">
          היי! נעים להכיר אני עדן ואני צליאקית שמאוהבת במתוקים! נכנסתי לעולם הקונדיטוריה במטרה להכיו דברים ללא גלוטן טובים ללא הבדל (:
        </p>
        <LangSwitcher class="mt-8" />
      </div>
     
      <div class="w-3/7 lg:w-auto">
        <div class="font-semibold mb-1">מוצרים</div>
        <div class="text-sm">
          <NuxtLink to="/products?orderby=date&order=DESC" class="py-1.5 block">{{ $t('messages.shop.newArrivals') }}</NuxtLink>
          <NuxtLink to="/products?filter=sale[true]" class="py-1.5 block">{{ $t('messages.shop.onSale') }}</NuxtLink>
          <NuxtLink to="/products?orderby=best-selling" class="py-1.5 block">{{ $t('messages.shop.productBestSellers') }}</NuxtLink>
          <a href="#" class="py-1.5 block">{{ $t('messages.shop.giftCards') }}</a>
        </div>
      </div>
      <div class="w-3/7 lg:w-auto">
        <div class="font-semibold mb-1">{{ $t('messages.general.customerService') }}</div>
        <div class="text-sm">
          <a href="#" class="py-1.5 block">צרו קשר</a>
          <a href="#" class="py-1.5 block">מדיניות משלוחים</a>
          <a href="#" class="py-1.5 block">מדיניות הפרטיות</a>
          <a href="#" class="py-1.5 block">תנאי שימוש</a>
        </div>
      </div>
      <div class="w-3/7 lg:w-auto">
        <div class="font-semibold mb-1">{{ $t('messages.account.myAccount') }}</div>
        <div class="text-sm">
          <NuxtLink to="/my-account" class="py-1.5 block">{{ $t('messages.account.myAccount') }}</NuxtLink>
          <NuxtLink to="/my-account?tab=orders" class="py-1.5 block">{{ $t('messages.shop.orderHistory') }}</NuxtLink>
          <NuxtLink to="/wishlist" class="py-1.5 block">{{ $t('messages.shop.wishlist') }}</NuxtLink>
          <a href="#" class="py-1.5 block">{{ $t('messages.general.newsletter') }}</a>
        </div>
      </div>
    </div>
    <div class="container border-t">
      <div class="copywrite">
        <p class="text-xs text-center py-4">
          WooNuxt v{{ runtimeConfig.public.version }} - by
          <a href="https://github.com/Orbitoly" target="_blank">Or Virt</a>
        </p>
      </div>
    </div>
  </div>
</template>
