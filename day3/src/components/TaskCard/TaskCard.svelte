<style>
  .task-card {
    position: relative;
    border-radius: 12px;

    margin: 20px 5px;
    box-sizing: border-box;
    padding: 16px;
    width: 100%;
    cursor: pointer;
    box-shadow: 2px 2px 4px 0px rgba(235, 235, 235, 1);
  }
  .task-card.yellow{
    background-color: var(--box-color);
  }
  .task-card.blue{
    background-color: var(--box-color-2);
  }
  .red{
    background-color: var(--box-color-3);
  }
  .green{
    background-color: var(--box-color-4);
  }
  h4 {
    margin: 0 0 0 0;
    opacity: 0.4;
    font-size: 10px;
  }
  h3 {
    font-size: 14px;
    font-weight: 500;
    opacity: 0.6;
  }
  .atendees {
    display: flex;
    margin-top: 14px;
  }
  img{
    border-radius: 50%;
    width: 30px;
    height: 30px;
    margin-right: 4px;
    object-fit: cover;
  }
</style>

<script>
  export let color
  export let time
  export let title
  export let srcs
  export let alt
</script>

<div class="task-card {color}">
  <h4>{time}</h4>
  <h3>{title}</h3>
  <div class="atendees">
    {#each Array(srcs.length) as _,i}
      <img src={srcs[i]} alt={alt[i]}/>
    {/each}
  </div>
</div>
