<script lang="ts">
  //TODO add imports to login, logout and get user state to replace the old function and variable
  import { user } from "$lib/store/user";
  import { signin, signout } from "$lib/services/authentication";

  // let loggedIn: boolean = false;

  // function login(): void {
  //   loggedIn = !loggedIn;
  // }
</script>

<!-- TODO replace loggedIn with a store variable and call correct function in on:click -->
<!-- {#if loggedIn}
  <button class="btn outline" on:click={login}>Logout</button>
{:else}
  <button class="btn outline" on:click={login}>Login</button>
{/if} -->

{#if $user}
  <button class="btn outline" on:click={signout}>Logout</button>
{:else}
  <button class="btn outline" on:click={signin}>Login</button>
{/if}

