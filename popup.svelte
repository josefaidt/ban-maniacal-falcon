<script lang="ts">
  import "@shoelace-style/shoelace"
</script>

<main>
  <section>
    <h1>my chrome extension</h1>
    <sl-card class="card-overview">
      <img
        slot="image"
        src="https://images.unsplash.com/photo-1559209172-0ff8f6d49ff7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=80"
        alt="A kitten sits patiently between a terracotta pot and decorative grasses." />

      <strong>Mittens</strong><br />
      This kitten is as cute as he is playful. Bring him home today!<br />
      <small>6 weeks old</small>

      <div slot="footer">
        <sl-button variant="primary" pill>More Info</sl-button>
        <sl-rating />
      </div>
    </sl-card>
  </section>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    font-size: 14px;
  }

  :global(body) {
    background-color: var(--sl-color-neutral);
  }

  :focus {
    outline: var(--c-tertiary) solid 1px;
  }

  main {
    --width: 320px;
    padding: 0.25rem;
    margin: 0 auto;

    width: var(--width);

    display: grid;
    grid-auto-columns: var(--width);
    grid-gap: 2rem;
  }

  main h1 {
    margin: 0;
    /* compensate for large grid gap */
    margin-bottom: -0.5rem;
  }

  sl-input::part(base):invalid {
    background: rgba(255, 99, 71, 0.1);
  }

  .card-overview {
    max-width: 300px;
  }

  .card-overview small {
    color: var(--sl-color-neutral-500);
  }

  .card-overview [slot="footer"] {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
