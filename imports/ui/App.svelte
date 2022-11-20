<script lang="ts">
  import Task from './Task.svelte';

  const getTasks = () => ([
    { _id: 'task1', text: 'This is task #1'},
    { _id: 'task2', text: 'This is task #2'},
    { _id: 'task3', text: 'This is task #3'},
    { _id: 'task4', text: 'This is task #4'},
  ])
</script>

<div class="container">
  <header>Todo List</header>

  <ul>
    {#each getTasks() as task (task._id)}
      <Task task={task} />
    {/each}
  </ul>
</div>
 