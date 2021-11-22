<template>
  <div class="wrap">
    <div class="header">header</div>
    <div class="content">
      <div class="block" v-for="(item, index) in [1,2,3,4,5,6,7,8,9]" :key="index">
        <div>{{item}}</div>
        <div><input type="text"></div>  
      </div>      
    </div>
    <div class="footer">footer</div>
  </div>
</template>

<script lang="ts">
  import { ref, defineComponent } from 'vue'
  export default defineComponent({
    name: 'Keyboard',
    props: {
      msg: {
        type: String,
        required: true
      }
    },
    setup: () => {
      const count = ref(0)
      return { count }
    }
  })
</script>

<style scoped>
  .wrap {
    display: flex;
    flex-direction: column;
    height: 100%;
    padding: 50px 0;
    box-sizing: border-box;
  }

  .content {
    flex: 1;
    overflow-y: auto;
  }

  .block {
    height: 300px;
    margin-bottom: 20px;
    background: #ccc;
  }

  .header, .footer {
    position: fixed;
    height: 50px;
    left: 0;
    right: 0;
    z-index: 1;
  }

  .header {
    top: 0;
    background: red;
  }

  .footer {
    bottom: 0;
    background: green;
  }

</style>