<script lang="ts">
  let rand: number = -1;

  function getRand() {
    fetch("./rand")
      .then((d) => d.text())
      .then((d) => (rand = parseInt(d)));
  }
</script>

<h1>Your number is {rand}!</h1>
<button on:click={getRand}>Get a random number</button>
