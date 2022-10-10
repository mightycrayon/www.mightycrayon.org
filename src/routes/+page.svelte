<script>
    import Statistic from "$lib/components/Statistic.svelte";

</script>
<div class="bg-img">
  <div class="caption">
    <h1>Art for Everyone</h1>
  </div>
</div>

<div class="row">
  <Statistic image="/top.png" number={5000} label="Crayons"></Statistic>  

  <div class="stat-description">
    <h1>Give me money</h1>
    It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy. Various versions have evolved over the years, sometimes by accident, sometimes on purpose (injected humour and the like).
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

  .row {
    display: flex;
    flex-direction: row;
  }

  .stat-description {
    flex: 3 1 0px;
    margin: 2vh;
  }
</style>