<style>
  .right-menu {
    display: flex;
    overflow: auto;
    width: 320px;
    border-left: 1px solid #e3e7f7;
    flex-direction: column;
  }
  p {
    display: relative;
    width: 100%;
    height: 40px;
    font-size: 26px;
    color: var(--main-color);
    margin: 70px 0 30px 30px;
  }
  .card-wrapper {
    position: relative;
    width: 100%;
    overflow-y: auto;
    box-sizing: border-box;
    padding: 10px 40px;
    flex: 1;
  }
</style>

<script>
  import TaskCard from '../TaskCard/TaskCard.svelte'
  let scheduledTasks = [
    {time: "08:00 - 09:00 AM", title: "Product Review", srcs: ["images/img1.jpg","images/img2.jpg","images/img3.jpg","images/img4.jpg"], alt: ["Member 1", "Member 2", "Member 3", "Member 4"], color: "yellow"},
    {time: "10:00 - 11:00 AM", title: "Design Meeting", srcs: ["images/img5.jpg","images/img6.jpg","images/img7.jpg"], alt: ["Member 1", "Member 2", "Member 3", "Member 4"], color: "blue"},// Wrong on purpose! :D
    {time: "01:00 - 02:00 PM", title: "Team Meeting", srcs: ["images/img1.jpg","images/img2.jpg","images/img3.jpg","images/img4.jpg"], alt: ["Member 1", "Member 2", "Member 3", "Member 4"],color: "red"},
    {time: "03:00 - 04:00 PM", title: "Release Event", srcs: ["images/img5.jpg","images/img6.jpg","images/img7.jpg","images/img9.jpg"], alt: ["Member 1", "Member 2", "Member 3", "Member 4"],color: "green"},
    {time: "11:00 - 12:00 PM", title: "Release Event", srcs: ["images/img5.jpg","images/img6.jpg","images/img7.jpg","images/img9.jpg"], alt: ["Member 1", "Member 2", "Member 3", "Member 4"],color: "yellow"}
  ]
  let color = ["yellow", "blue", "red", "green"]
</script>

<div class="right-menu">
  <div>
    <p>Schedule</p>
    <div class="card-wrapper ">
      {#each scheduledTasks as { time, title, srcs, alt, color }}
        <TaskCard {time} {title} {srcs} {alt} {color}/>
      {/each}
    </div>
  </div>
</div>
