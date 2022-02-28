<style>
  ul {
    list-style-type: none;
    padding: 0;
  }

  .feather {
    width: 14px;
    height: 14px;
    color: currentColor;
    margin-right: 10px;
  }

  .item {
    display: flex;
    align-items: center;
    color: var(--main-color);
    font-weight: 500;
    margin-bottom: 14px;
  }

  .left-content {
    padding: 40px;
  }

  .category-list {
    margin-top: 50px;
  }

  .category-list .item {
    color: var(--secondary-color);
  }
</style>

<script>
  export let actionItems
  export let categoryItems
</script>

<div class="left-bar">
  <div class="upper-part">
    <div class="actions">
      <div class="circle" />
      <div class="circle-2" />
    </div>
  </div>

  <div class="left-content">
    <ul class="action-list">
      {#each actionItems as item}
        <li class="item">
          <img class="feather" src={item.src} alt={item.alt} />
          <span>{item.description}</span>
        </li>
      {/each}
    </ul>

    <ul class="category-list">
      {#each categoryItems as item}
        <li class="item">
          <img class="feather" src={item.src} alt={item.alt} />
          <span>{item.description}</span>
        </li>
      {/each}
    </ul>
  </div>
</div>
