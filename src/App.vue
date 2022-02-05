<template>
  <div>
    <MyComponent />
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap-icons/font/bootstrap-icons.css'
import MyComponent from './components/MyComponent.vue';

export default {
  name: 'App',
  components: {
    MyComponent,
  },
};
</script>
