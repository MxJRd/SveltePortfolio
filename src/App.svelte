<script lang="ts">
  import Header from "./components/Header.svelte";
  import { MaterialApp, Container, Row, Col } from "svelte-materialify/src";
  import ContactMe from "./components/ContactMe.svelte";
  import Projects from "./components/Projects.svelte";
  import AboutMe from "./components/AboutMe.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  const theme = "dark";
</script>

<main>
  <MaterialApp {theme}>
    <Container>
      <Col>
        <Sidebar />
      </Col>
      <Col>
        <Header />
        <AboutMe />
        <Projects />
        <ContactMe />
      </Col>
    </Container>
  </MaterialApp>
</main>

<style>
  :global(body.dark-theme)
  main {
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
