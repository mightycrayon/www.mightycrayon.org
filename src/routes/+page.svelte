<div class="bg-img">
  <div class="caption">
    <h1>Art for Everyone</h1>
  </div>
</div>

<div class="stats">
  <div class="stat">
    400 Crayons
  </div>
</div>

<style>
  .bg-img {
    background-image: url("/top.png");
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    width: 100%;
    height: calc(100vh - 2em);
    margin: 0;
  }

  .caption {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .caption h1 {
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    padding: 2vh;
  }

  .stats {
    display: flex;
    flex-direction: row;
    margin: 2vh;
  }

  .stat {
    border-radius: 100%;
    background-color: rgba(0, 0, 255, 0.5);
  
    width: 21vw;
    height: 21vw;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>