<template>
  <form @submit.prevent="cadastraTarefa">
    <div class="row">
      <div class="col">
        <input :value="estado.tarefaTemp" @change="evento => estado.tarefaTemp = evento.target.value" required
          class="form-control" type="text" placeholder="Digite aqui a descrição da tarefa">
      </div>

      <div class="col-md-1">
        <button type="submit" class="btn btn-primary">Cadastrar</button>
      </div>
    </div>

    <div class="col-md-2">
      <select @change="evento => estado.filtro = evento.target.value" class="form-control">
        <option value="todas">Todas tarefas</option>
        <option value="pendentes">Tarefas Pendentes</option>
        <option value="finalizadas">Tarefas Finalizadas</option>

      </select>
    </div>

  </form>
</template>