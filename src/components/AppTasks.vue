<template>
  <div class="container">
    <div class="row">
      <div class="col-6">
        <h3>New Task</h3>
        <input class="form-control mb-2" type="text" placeholder="Task...">
        <input class="form-control mb-2" type="number" placeholder="Hours...">
        <button class="btn btn-primary btn-sm">Guardar</button>
        <button class="btn btn-danger btn-sm">Cancelar</button>
      </div>
      <div class="col-6">
        <h3>List Task</h3>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'AppTasks',
  data () {
    return {
    }
  }
}
</script>
