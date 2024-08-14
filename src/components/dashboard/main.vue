<template>
  <div class="mt-4">
    <v-card class="pa-4">
    <v-text-field class="pt-4"
    label="Task Name"
    v-model="task_name"
    >

    </v-text-field>
    <v-textarea
      class="pt-4"
      label="Task Description"
      v-model="task_description"
      >

    </v-textarea>
    <v-btn class="my-button" @click="Add_task">+ Add Task</v-btn>
  </v-card>
  <v-card
    class="task_details"
  >
    
  </v-card>
  </div>

</template>

<script setup>
import axios  from 'axios';
import { ref}  from 'vue'
const task_name = ref("")
const task_description = ref("")


function Add_task(){
  console.log("task name : ",task_name.value)
  console.log("Task description : ",task_description.value)
}

</script>


<style scoped>
.mt-4{
  margin: auto;

  width: 50%;
  height: 25%;

}
.pt-4{
  padding-left: 10px;
  padding-right: 10px;
}
.my-button{
  background-color: rgb(61, 240, 106);

  margin-left: 10px;
}
</style>
