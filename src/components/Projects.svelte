<script lang="ts">
  import { Tabs, Tab, TabContent, Button, Icon } from "svelte-materialify";
  import { mdiPageFirst } from "@mdi/js";
  const projectsArray = ["Typequest", "hopLiteJS", "CodesmithFund"];
</script>

<section>
  <Tabs vertical>
    <div slot="tabs">
      {#each Array(3) as _, i}
        <Tab class="primary-color rounded-r-xl">{projectsArray[i]}</Tab>
      {/each}
      <Button fab size="small">
        <Icon path={mdiPageFirst} />
      </Button>
    </div>

    <div class="pa-2">
      {#each Array(5) as _, i}
        <TabContent>
          Item Content
          {i + 1}
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
            accumsan, diam et elementum gravida, arcu mi fermentum nibh, vel
            dapibus ligula orci non est. Morbi commodo sagittis finibus.
            Maecenas in volutpat massa. Nullam vulputate metus velit, quis
            interdum elit imperdiet ut. Suspendisse et sagittis erat, euismod
            vulputate enim. Etiam feugiat sit amet justo vitae commodo.
          </p>
        </TabContent>
      {/each}
    </div>
  </Tabs>
  <hr />
</section>

<style>
  section {
    height: 50vh;
  }
</style>
