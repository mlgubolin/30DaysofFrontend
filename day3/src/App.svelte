<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap');

  * {
    box-sizing: border-box;
    outline: none;
  }
  :root {
    --bg-color: #f5f8ff;
    --main-color: #353536;
    --secondary-color: #8e92a4;
    --main-text-color: #5d606b;
    --secondary-dark-color: #9496a5;
    --tag-color-one: #e0fbf6;
    --tag-color-text-one: #58c2a9;
    --tag-color-two: #ece7fe;
    --tag-color-text-two: #8972f3;
    --tag-color-three: #fde7ea;
    --tag-color-text-three: #e77f89;
    --tag-color-four: #f7f8fc;
    --tag-color-text-four: #a0a6b5;
    --checkbox-color: #009e90;
    --button-color: #49beb7;
    --box-color: #fff1d6;
    --box-color-2: #d3e6ff;
    --box-color-3: #ffd9d9;
    --box-color-4: #daffe5;
    --task-color: #777982;
  }

  body {
    display: flex;
    align-items: center;
    margin: 0;
    justify-content: center;
    flex-direction: column;
    overflow: auto;
    width: 100%;
    height: 100vh;
    padding: 20px;
    font-family: 'DM Sans', sans-serif;
    font-size: 12px;
    background-image: linear-gradient(
        21deg,
        rgba(64, 83, 206, 0.3697003234675773) 68%,
        rgba(255, 206, 196, 0.5) 163%
      ),
      linear-gradient(
        163deg,
        rgba(49, 146, 170, 0.07944489965716128) 86%,
        rgba(239, 112, 138, 0.5) 40%
      ),
      linear-gradient(
        30deg,
        rgba(76, 79, 173, 0.6173675716587805) 22%,
        rgba(237, 106, 134, 0.5) 169%
      ),
      linear-gradient(
        48deg,
        rgba(31, 85, 147, 0.7323890641868473) 64%,
        rgba(247, 126, 132, 0.5) 43%
      );
    background-blend-mode: overlay, multiply, color, normal;
  }

  .task-manager {
    display: flex;
    justify-content: space-between;
    width: 100%;
    max-width: 1200px;
    height: 90vh;
    max-height: 900px;
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 0.3px 2.2px rgba(0, 0, 0, 0.011), 0 0.7px 5.3px rgba(0, 0, 0, 0.016),
      0 1.3px 10px rgba(0, 0, 0, 0.02), 0 2.2px 17.9px rgba(0, 0, 0, 0.024),
      0 4.2px 33.4px rgba(0, 0, 0, 0.029), 0 10px 80px rgba(0, 0, 0, 0.04);
    overflow: hidden;
  }
</style>

<script>
  import LeftMenu from './components/LeftMenu/Leftmenu.svelte'
  import Task from './components/Task/Task.svelte'
  import TaskCard from './components/TaskCard/TaskCard.svelte'
  import TaskFrame from './components/TaskFrame/TaskFrame.svelte'

  let actionItems = [
    { src: 'svg/inbox.svg', alt: 'Inbox', description: 'Inbox' },
    { src: 'svg/star.svg', alt: 'Today', description: 'Today' },
    { src: 'svg/calender.svg', alt: 'Upcoming', description: 'Upcoming' },
    { src: 'svg/hash.svg', alt: 'Important', description: 'Important' },
    { src: 'svg/users.svg', alt: 'Meetings', description: 'Meetings' },
    { src: 'svg/trash.svg', alt: 'Trash', description: 'Trash' }
  ]

  let categoryItems = [
    { src: 'svg/users.svg', alt: 'Family', description: 'Family' },
    { src: 'svg/sun.svg', alt: 'Vacations', description: 'Vacations' },
    { src: 'svg/trending.svg', alt: 'Festivals', description: 'Festivals' },
    { src: 'svg/zap.svg', alt: 'Concerts', description: 'Concerts' }
  ]
</script>

<html lang="en">
  <body>
    <div class="task-manager">
      <LeftMenu {actionItems} {categoryItems} />
      <TaskFrame />
    </div>
  </body>
</html>
