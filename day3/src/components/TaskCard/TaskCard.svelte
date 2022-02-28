<script>
  import Task from '../Task/Task.svelte'
  export let tasks
</script>

<!-- <title />
<div class="categories" /> -->
<div class="task-wrapper">
  {#each tasks as { title, url, tag, checked }}
    <Task {title} {url} {tag} {checked} />
  {/each}
</div>
