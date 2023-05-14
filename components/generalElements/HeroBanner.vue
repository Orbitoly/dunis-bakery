<template>
  <div class="mx-auto relative">
    <div dir="rtl" class="container bg-gradient-to-l flex flex-col from-gray-100 inset-0 text-gray-800 absolute items-start justify-center md:bg-none md:p-12 lg:p-24">
      <h1 class="font-bold text-white text-3xl md:mb-4 md:text-4xl lg:text-6xl">ללא גלוטן - התחלנו!</h1>
      <h2 class="font-bold text-white text-lg md:mb-4 lg:text-3xl">תפריט שבועות</h2>
      <div class="font-light text-white max-w-sm text-sm mb-8 lg:max-w-md">
        בואו לגלות את העולם החדש של האוכל ללא גלוטן - במיוחד לשבועות!
      </div>
      <NuxtLink class="rounded-xl font-bold bg-gray-800 text-white py-4 px-8 hover:bg-gray-800" to="/products">לרכישה</NuxtLink>
    </div>
    <img
      width="1400"
      height="800"
      class="object-cover h-[360px] w-full md:h-[420px] lg:h-[560px] xl:h-[640px]"
      src="/images/shavoot.jpeg"
      alt="Hero image"
      loading="eager"
      format="webp"
      fit="outside"
      sizes="sm:100vw lg:1400px" />
  </div>
</template>
