<script lang="ts">
    import { onMount } from 'svelte';
  
    export let inputString = '';
    let encodedString = '';
  
    function handleEncode() {
      encodedString = btoa(inputString);
    }
  
    function handleCopy() {
      navigator.clipboard.writeText(encodedString);
    }
  
    onMount(() => {
      console.log('Component mounted.');
    });
  </script>
  
  <input bind:value={inputString} />
  <button on:click={handleEncode}>Encode</button>
  <br />
  <p>Encoded String: {encodedString}</p>
  <button on:click={handleCopy}>Copy</button>