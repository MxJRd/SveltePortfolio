<script>
  import NavBar from "./NavBar.svelte";
  import { Button, Container, Row, Col } from "svelte-materialify/src";
</script>

<div>
  <head>
    <title>Maxwell J. Reed</title>
  </head>
  <body>
    <header>
      <NavBar />
      <Container>
        <h1>The Efficient <span><strong>Unorthodox</strong></span></h1>
        <h4>My Journey through Learning to Code</h4>
        <br />
        <Button class="secondary-color">Welcome</Button>
      </Container>
      <hr />
    </header>
    <article>
      <header>
        <h2>About Me</h2>
        <p>Who I am</p>
      </header>
    </article>
  </body>
</div>

<style>
</style>