<template>
  <main class="flex justify-center dark:bg-gray-300 min-h-screen p-4 bg-gray-50 overflow-y-hidden">
    <div class="max-w-5xl w-full flex bg-white h-full p-5 rounded-lg shadow-lg">
      <div>
        <h1>{{ greet }} {{ message }}</h1>
        <h1 v-text="name"></h1>
        <h1 v-html="boldText"></h1>
        <h2 :id="headingId">This is a heading</h2>
        <h1 :style="{
          color: highlight,
          fontSize: headerSize + 'px',
        }">Instyle Style</h1>
        <h1 :style="styleObject">Style Object</h1>
        <button :disabled="isDisabled" class="bg-gray-300 p-2 rounded-lg">Disabled</button>
        <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
        <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
      </div>
    </div>
  </main>
</template>


<script>

export default {
  name: 'App',
  data() {
    return {
      message: 'Vue!',
      greet: "Hello",
      name: "Sahil",
      boldText: "<b>This is a bold text</b>",
      headingId: "heading",
      isDisabled: true,
      highlight: "orange",
      headerSize: 100,
      styleObject: {
        color: 'red',
        fontSize: '100px',
        textDecoration: "bold"
      },
      baseStyleObject: {
        fontSize: '100px',
        padding: '5px',
        margin: '5px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',
        borderRadius: '5px',
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor: 'lightcoral',
        border: '1px solid red',
        borderRadius: '5px',
      }
    }
  }
}
</script>