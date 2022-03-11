<style>
  .task-frame {
    display: flex;
    flex-direction: column;
    overflow: auto;
    flex-grow: 1;
    padding: 40px 20px 0 20px;
  }
  p {
    font-size: 26px;
    color: var(--main-color);
    margin-top: 30px;
  }
  .tabs {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
    border-bottom: 1px solid #ddd;
    margin-bottom: 15px;
  }
  .tabs span {
    font-weight: 500;
    color: var(--secondary-color);
    border-bottom: 1px solid #ddd;
    transition: 0.4s ease-in;
    padding: 20px 30px;
    cursor: pointer;
  }
</style>

<script>
  import Task from '../Task/Task.svelte'

  import TaskCard from '../TaskCard/TaskCard.svelte'

  let todayTasks = [
    { title: 'Dashboard Design Implementation', url: '', tag: 'Approved', checked: true },
    { title: 'Create a userflow', url: '', tag: 'In Progress', checked: true },
    { title: 'Application Implementation', url: '', tag: 'In Review', checked: false },
    { title: 'Create a Dashboard Design', url: '', tag: 'In Progress', checked: false },
    {
      title: 'Create a Web Application Design',
      url: '',
      tag: 'Approved',
      checked: false
    },
    { title: 'Interactive Design', url: '', tag: 'In Review', checked: false }
  ]

  let upcomingTasks = [
    { title: 'Dashboard Design Implementation', url: '', tag: 'Waiting', checked: false },
    { title: 'Create a userflow', url: '', tag: 'Waiting', checked: false },
    { title: 'Application Implementation', url: '', tag: 'Waiting', checked: false },
    { title: 'Create a Dashboard Design', url: '', tag: 'Waiting', checked: false }
  ]
</script>

<div class="task-frame">
  <p>Today Tasks</p>
  <div class="tabs">
    <span>All</span>
    <span>Important</span>
    <span>Notes</span>
    <span>Links</span>
  </div>
  <div class="task-wrapper">
    {#each todayTasks as { title, url, tag, checked }}
      <Task {title} {url} {tag} {checked} />
    {/each}
  </div>

  <p>Upcoming Tasks</p>
  <div class="tabs" />
  <div class="task-wrapper">
    {#each upcomingTasks as { title, url, tag, checked }}
      <Task {title} {url} {tag} {checked} />
    {/each}
  </div>
</div>
