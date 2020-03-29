<template>
  <div class="max-w-sm w-full lg:max-w-full lg:flex">
    <div
      class="h-48 lg:h-auto lg:w-48 flex-none bg-cover rounded-t lg:rounded-t-none lg:rounded-l text-center overflow-hidden"
      :style="url"
      title="title"
    ></div>
    <div
      class="border-r border-b border-l border-gray-400 lg:border-l-0 lg:border-t lg:border-gray-400 bg-white rounded-b lg:rounded-b-none lg:rounded-r p-4 flex flex-col justify-between leading-normal"
    >
      <div class="mb-8">
        <p class="text-sm text-gray-600 flex items-center">
          <slot name="kicker"/>
        </p>
        <div class="text-gray-900 font-bold text-xl mb-2">
          <slot name="main"/>
        </div>
        <p class="text-gray-700 text-base">
          <slot name="bottom"/>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['url']
}
</script>
