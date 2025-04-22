<template>
  <main class="flex justify-center dark:bg-gray-300 min-h-screen p-4 bg-gray-50 overflow-y-hidden">
    <div class="max-w-5xl w-full flex bg-white h-full p-5 rounded-lg shadow-lg">
      <div>
        <h1 v-if="num === 5"> This is number <span span class=" text-2xl text-green-500"> {{ num }} </span>
        </h1>
        <h1 v-else-if="num > 5">It is greater than five. The number is <span class="text-2xl text-green-500"> {{
          num }} </span> </h1>
        <h1 v-else-if="num < 5">It is less than five. The number is <span class="text-2xl text-green-500"> {{
          num }} </span> </h1>
        <h1 v-else><span class="text-2xl text-red-500">Please choose a number. Not "{{ num }}" </span>.
        </h1>
        <template v-if="display">
          <h1 class="text-2xl text-gray-300">This is a hidden message</h1>
        </template>
      </div>
    </div>
  </main>
</template>


<script>
export default {
  name: 'App',
  data() {
    return {
      num: "Hello",
      display: true,
    }
  }
}
</script>