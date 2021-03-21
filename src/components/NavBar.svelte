<script>
  import {
    AppBar,
    Button,
    Icon,
    Menu,
    ListItem,
  } from "svelte-materialify/src";
  import { mdiMenu, mdiDotsVertical } from "@mdi/js";
</script>

  <AppBar class="primary-color">
    <div slot="icon">
      <Button fab size="small">
        <Icon path={mdiMenu} />
      </Button>
    </div>
    <span slot="title">Title</span>
    <div style="flex-grow:1" />
    <Button>Item</Button>
    <Menu right>
      <div slot="activator">
        <Button fab size="small">
          <Icon path={mdiDotsVertical} />
        </Button>
      </div>
      <ListItem>Item 1</ListItem>
      <ListItem>Item 2</ListItem>
      <ListItem>Item 3</ListItem>
    </Menu>
  </AppBar>
