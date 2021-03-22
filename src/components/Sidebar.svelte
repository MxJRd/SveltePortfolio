<script lang="ts">
  import {
    NavigationDrawer,
    List,
    ListItem,
    Avatar,
    Divider,
    Icon,
  } from "svelte-materialify";
  import {
    mdiHomeCity,
    mdiAccount,
    mdiBookMinusMultiple,
    mdiAccountSupervisorCircleOutline,
    mdiContacts,
  } from "@mdi/js";

  let mini = true;
  function naventer() {
    mini = false;
  }
  function navleave() {
    mini = true;
  }
    let item1: boolean = true;
      let item2: boolean = true;
      let item3: boolean = true;
      let item4: boolean = true;
    function item1Hover() {
      item1 = false;
    }
    function item1Exit() {
      item1 = true;
    }
    function item2Hover() {
      item2 = false;
    }
    function item2Exit() {
      item2 = true;
    }
    function item3Hover() {
      item3 = false;
    }
    function item3Exit() {
      item3 = true;
    }
    function item4Hover() {
      item4 = false;
    }
    function item4Exit() {
      item4 = true;
    }
</script>

<div
  class="d-inline-block"
  id="nav-drawer"
  on:mouseenter={naventer}
  on:mouseleave={navleave}
>
  <NavigationDrawer fixed {mini}>
    <ListItem class="primary-color" slot="prepend">
      <span slot="prepend" class="ml-n2">
        <Avatar size={40}>
          <img src="//picsum.photos/200" alt="profile" />
        </Avatar>
      </span>
      Maxwell J. Reed
    </ListItem>
    <Divider />
    <List dense nav>
      <div on:mouseenter={item1Hover} on:mouseleave={item1Exit}>
        <ListItem ripple={false} class={item1 ? "primary-color" : "secondary-color"}>
          <span slot="prepend">
            <Icon path={mdiHomeCity} />
          </span>
          Home
        </ListItem>
      </div>
      <div on:mouseenter={item2Hover} on:mouseleave={item2Exit}>
        <ListItem ripple={false} class={item2 ? "primary-color" : "secondary-color"}>
          <span slot="prepend">
            <Icon path={mdiAccountSupervisorCircleOutline} />
          </span>
          About Me
        </ListItem>
      </div>
      <div on:mouseenter={item3Hover} on:mouseleave={item3Exit}>
      <ListItem ripple={false} class={item3 ? "primary-color" : "secondary-color"}>
        <span slot="prepend">
          <Icon path={mdiBookMinusMultiple} />
        </span>
        Projects
      </ListItem>
    </div>
    <div on:mouseenter={item4Hover} on:mouseleave={item4Exit}>
      <ListItem ripple={false} class={item4 ? "primary-color" : "secondary-color"}>
        <span slot="prepend">
          <Icon path={mdiContacts} />
        </span>
        Contact Me
      </ListItem>
    </div>
    </List>
  </NavigationDrawer>
</div>

<style>
</style>
