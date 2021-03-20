<script>
    let second;
    function blockHandler(event) {
        if (
            event.target.id == "red" ||
            event.target.id == "blue" ||
            event.target.id == "green"
        ) {
            event.target.style.visibility = "hidden";
        } else {
            for (let block of second.children) {
                block.style.visibility = "visible";
            }
        }
    }
</script>

<p>Второй компонент.</p>
<div id="second" bind:this={second} on:click={blockHandler}>
    <div class="block" id="red" />
    <div class="block" id="blue" />
    <div class="block" id="green" />
</div>

<style>
    .block {
        display: inline-block;
        margin-top: 10px;
        height: 100px;
        width: 100px;
    }
    #red {
        background-color: red;
    }
    #blue {
        background-color: blue;
    }
    #green {
        background-color: green;
    }
</style>
