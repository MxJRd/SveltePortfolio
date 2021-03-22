<script lang="ts">
    import {
      mdiLinkedin,
      mdiEmailVariant,
      mdiInstagram,
      mdiGithub,
    } from "@mdi/js";
    import { Button, Icon } from "svelte-materialify/src";
  </script>
  
  <section>
    <h2>Contact Me</h2>
    <p>LinkedIn</p>
    <Button fab size="small">
      <Icon path={mdiLinkedin} />
    </Button>
    <p>Github</p>
    <Button fab size="small">
      <Icon path={mdiGithub} />
    </Button>
    <p>Email</p>
    <Button fab size="small">
      <Icon path={mdiEmailVariant} />
    </Button>
    <p>Instagram</p>
    <Button fab size="small">
      <Icon path={mdiInstagram} />
    </Button>
    <hr />
  </section>
  