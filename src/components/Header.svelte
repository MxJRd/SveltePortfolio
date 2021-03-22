<script lang="ts">
  import NavBar from "./NavBar.svelte";
  import { Button, Container, Row, Col, Overlay } from "svelte-materialify/src";
  // import
</script>

<section>
  <head>
    <title>Maxwell J. Reed</title>
  </head>
  <header>
    <!-- <NavBar /> -->
    <Container>
      <h1>
        The Efficient <span class="pink-text text-darken-1"
          ><strong>Unorthodox</strong></span
        >
      </h1>
      <h4>
        My Journey through <strong
          ><span class="light-green-text text-accent-4">Fullstack</span> Development</strong
        >
      </h4>
      <br />
      <p>Enjoy your Stay.</p>
      <Button class="secondary-color">Welcome</Button>
    </Container>
    <hr />
  </header>
</section>

<style>
  header {
    height: 100vh;
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }
</style>
