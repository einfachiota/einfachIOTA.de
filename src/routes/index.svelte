<style>
  .home-container {
    align-items: center;
    display: flex;
    flex: 1;
    justify-content: center;
    margin: 2em 0;
    min-height: 400px;
  }

  .home-copy {
    flex: 1;
  }

  .hallo {
    text-decoration: underline #00B8C5;
  }

  h1 {
    font-weight: 700;
    margin-bottom: 0.5em;
  }

  p {
    font-size: 1.4em;
    line-height: 1.5;
  }

  figure {
    margin: 0 1em;
    text-align: center;
  }

  img {
    width: 100%;
    max-width: 400px;
  }

  @media (max-width: 1020px) {
    p {
      font-size: 1.2em;
    }

    img {
      max-width: 300px;
    }
  }

  @media (max-width: 800px) {
    .home-container {
      flex-direction: column;
    }

    .home-copy {
      flex: 0;
      padding-bottom: 2em;
      text-align: center;
    }
  }
</style>

<svelte:head>
  <title>einfachIOTA</title>
</svelte:head>

<div class="home-container">
  <div class="home-copy">
    <h1 class="hallo">Hallo!</h1>
    <p>Willkommmen bei einfachIOTA!</p>
    <p>Hier bekommst du alles rund um IOTA einfach erklärt!</p>
  </div>

  <figure>
    <img alt='Person typing on laptop' src='undraw-illustration.svg'>
  </figure>
</div>
