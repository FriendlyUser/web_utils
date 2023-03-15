<script lang="ts">
    export let value = "";

    function reverseString() {
        value = value.split("").reverse().join("");
    }
</script>

<div>
    <input type="text" bind:value />
    <button on:click={reverseString}>Reverse</button>
    <p>Reversed: {value}</p>
</div>