<script lang="ts">
  import { onMount } from "svelte";

  export let image: string;
  export let number: number;
  export let label: string;

  let numberval = number;

  let options: IntersectionObserverInit = {
    root: null,
    rootMargin: "0px",
    threshold: 0.5,
  }

  let time = 50;


  function updateNumberVal() {
    numberval++;
    time += 5;
    if (numberval < number) {
      setTimeout(updateNumberVal, time);
    } else {
      numberval = number;
    }
  }

  function observerHandler(entries: IntersectionObserverEntry[], observer: IntersectionObserver) {
    entries.forEach((entry: IntersectionObserverEntry) => {
      if (entry.isIntersecting) {
        // Start number counting
        numberval = Math.round(number - 25);
        time = 100;
        setTimeout(updateNumberVal, time);
      }
    });
  }

  let el: HTMLElement;

  onMount(() => {
    let observer = new IntersectionObserver(observerHandler, options);
    observer.observe(el);
  });
</script>

<div class="stat" style:background-image={"url(" + image + ")"} bind:this={el}>
  <div class="stat-bubble">
    {numberval} {label}
  </div>
</div>

<style>
  .stat-bubble {
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    border-radius: 100%;
    background-color: rgba(34, 180, 245, 0.75);
    color: white;
  
    width: 20vh;
    height: 20vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .stat {
    background-size: cover;
    flex: 2 1 0px;

    margin: 2vh;
  }
</style>