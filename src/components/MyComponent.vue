<template>
  <div class="container">
    <h1>My Component</h1>
    <div class="input-group mb-2">
      <input
        type="text"
        placeholder="Add task"
        class="form-control"
        v-model="task"
        v-on:keyup.enter="addTask(task)"
      />
      <button class="btn btn-primary" v-on:click="addTask(task)">
        <i class="bi bi-arrow-return-left"></i>
      </button>
    </div>
    <ul class="list-group">
      <li class="list-group-item" v-for="task in tasks" v-bind:key="task">
        <div class="row">
          <div class="col-md-8 col-10">
            {{ task }}
          </div>
          <div class="col-md-4 col-2">
            <button type="button" class="btn btn-danger" v-on:click="removeTask(task)">
              <i class="bi bi-trash"></i>
            </button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
// start here
export default {
  name: 'MyComponent',
  props: {
    msg: String,
  },
  data() {
    return {
      tasks: ['Go somwhere', 'Do this', 'Do that'],
    };
  },

  methods: {
    addTask(task) {
      this.tasks.push(task);
      this.task = '';
    },
    removeTask(task) {
      this.tasks.splice(this.tasks.indexOf(task), 1);
    }
  },
  created() {
  }
};
</script>
