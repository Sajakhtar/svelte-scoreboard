<script>
  import Navbar from './Navbar.svelte';
  import Player from './Player.svelte';

  let players = [
    {name: 'Jon Snow', points: 113},
    {name: 'Karl Drogo', points: 46},
    {name: 'Khalesee', points: 174}
  ];
</script>



<Navbar />
<div class="container">
  {#if players.length === 0}
    <p>No Players</p>
  {:else}
    {#each players as player}
      <Player name={player.name} points={player.points} />
    {/each}
  {/if}
</div>
