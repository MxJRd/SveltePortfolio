<script>
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
  let itemHover = true;

  function itemEnter() {
    itemHover = false;
  }
  function itemLeave() {
    itemHover = true;
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
      <div on:mouseenter={itemEnter} on:mouseleave={itemLeave}>
        <ListItem class={itemHover ? "primary-color" : "secondary-color"}>
          <span slot="prepend">
            <Icon path={mdiHomeCity} />
          </span>
          Home
        </ListItem>
      </div>
      <div on:mouseenter={itemEnter} on:mouseleave={itemLeave}>
        <ListItem class={itemHover ? "primary-color" : "secondary-color"}>
          <span slot="prepend">
            <Icon path={mdiAccountSupervisorCircleOutline} />
          </span>
          About Me
        </ListItem>
      </div>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiBookMinusMultiple} />
        </span>
        Projects
      </ListItem>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiContacts} />
        </span>
        Contact Me
      </ListItem>
    </List>
  </NavigationDrawer>
</div>

<style>
</style>
