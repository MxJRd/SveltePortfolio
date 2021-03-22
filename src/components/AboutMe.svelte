<script lang="ts">
    let stepOneMessage = "?????";
    let count = 0;
    function messageClicked() {
        switch(count) {
            case 0: 
                count += 1;
                stepOneMessage = "PANIC"
                break;
            case 1: 
                stepOneMessage = "Please stop."
                count += 1;
                break;
            case 2: 
                stepOneMessage = "Please no."
                count += 1;
                break;
            case 3: 
                stepOneMessage = "Pretty please?"
                count += 1;
                break;
            case 4: 
                stepOneMessage = "BACK TO SQUARE ONE."
                count += 1;
                break;
            case 5: 
                stepOneMessage = "?????"
                count = 0;
                break;
        }
    }
    let messageHovered = true;
    function messageHover() {
        messageHovered = false;
    }
    function messageExit () {
        messageHovered = true;
    }
</script>

<article>
  <h2>About Me</h2>
  <p></p>
  <p>"Plan? Pfft, I've always got a plan! <strong>Step One: <span on:click={messageClicked} class="pink-text text-darken-1"><span on:mouseenter={messageHover} on:mouseleave={messageExit} class={messageHovered ? "grey darken-4" : "primary-color"}>{stepOneMessage}</span></span></strong></p>
  <p></p>
  <p>Who I am</p>
  <hr />
</article>

<style>
  article {
    height: 50vh;
  }
</style>
