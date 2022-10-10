<svelte:head>
  <title>Mighty Crayon</title>
</svelte:head>

<div class="navbar">
  <a class="navbar-item navbar-title navbar-link" href="/">Mighty Crayon</a>
  <div style="flex-grow: 1;"></div>
  <a href="/hi" class="navbar-item navbar-link">Hi</a>
</div>

<slot></slot>

<style>
  :global(body) {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  .navbar {
    background-color: #333;
    width: 100%;
    position: sticky;
    top: 0px;
    display: flex;
    flex-direction: row;
    color: white; 
    align-items: center;
  }

  .navbar-item {
    margin: 1vw;
  }

  .navbar-link {
    text-decoration: none;
    color: #aaa;
  }

  .navbar-title {
    color: white;
    font-size: 2em;
    font-weight: bold;
  }
</style>