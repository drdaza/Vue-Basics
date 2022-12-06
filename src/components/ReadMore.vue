<script setup>
import { ref, computed } from "vue";
  let count = ref(0);
  const title = ref("Exercise Read More");

  function changeClass(){
    (count.value == 0) ? count.value = 1 : count.value = 0;
  }
  
  let change = computed(()=>{
    return{
        'cut-text': count.value == 0,
        '': count.value == 1
    }
  })
  

</script>

<template>
  <div class="container text-center">
    <h1 class="my-3">{{ title }}</h1>
    <div>
      <p :class="['mb-3', 'd-block',change]">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos
        ipsa neque odio consectetur impedit tempore modi accusantium! Voluptatem
        molestiae nemo inventore soluta corrupti. Culpa perferendis sapiente
        deserunt aperiam maxime consectetur recusandae quasi commodi dicta
        temporibus pariatur ab repellendus dignissimos natus aliquam odit ullam,
        quaerat autem non hic, quidem dolore laboriosam.
      </p>
      <button class="btn btn-primary" @click="changeClass()">Show More</button>
    </div>
    <hr class="mb-4" />
  </div>
</template>

<style lang="css"></style>
