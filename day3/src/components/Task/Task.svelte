<style>
  a {
    display: flex;
    position: relative;
    justify-content: flex-start;
    margin-bottom: 10px;
    padding-left: 30px;
    color: var(--task-color);
    font-size: 13px;
    font-weight: 500;
  }
  input {
    height: 18px;
  }
  label {
    margin: 0 40px 0 12px;
  }
  span {
    font-size: 10px;
    padding: 5px 8px;
    border-radius: 20px;
  }
  span.Approved {
    background-color: var(--tag-color-one);
    color: var(--tag-color-text-one);
  }
  span.Progress {
    background-color: var(--tag-color-two);
    color: var(--tag-color-text-two);
  }
  span.Review {
    background-color: var(--tag-color-three);
    color: var(--tag-color-text-three);
  }
  span.Waiting {
    background-color: var(--tag-color-four);
    color: var(--tag-color-text-four);
  }
</style>

<script>
  export let title
  export let url
  export let tag
  export let checked
</script>

<a href={url}>
  <input type="checkbox" id="scales" name="title" {checked} />
  <label for="title">{title}</label>
  <span class={tag}> {tag}</span>
</a>
