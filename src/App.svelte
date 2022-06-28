<script>
// @ts-ignore
import Facebook from "./lib/Facebook.svelte";

import GoogleSignInButton from "./lib/GoogleSignInButton.svelte";


  
</script>

<main>
  <GoogleSignInButton/>
  <Facebook/>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }
</style>
