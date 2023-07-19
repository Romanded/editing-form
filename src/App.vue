<template>
    <div>
        <EditingForm/>
    </div>
</template>

<script>

import EditingForm from "@/components/EditingForm.vue";

export default {
  name: 'App',
  components: {
      EditingForm
  }
}
</script>

<style>
  * {
    font-family: sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  div {
      width: 100vw;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
  }

</style>
