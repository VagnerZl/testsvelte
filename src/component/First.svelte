<script>
    let firstb;
    function colorChange(event) {
        console.log(event.target.value, firstb);
        firstb.style.backgroundColor = `${event.target.value}`;
    }
    function opacityChange(event) {
        console.log(event.target.value, firstb);
        firstb.style.opacity = `${event.target.value}`;
    }
</script>

<p>Первый компонент.</p>
<label>
    Выбери цвет: <input on:input={colorChange} type="color" value="#000000" />
</label>
<label>
    Выбери прозрачность: 0%
    <input
        on:input={opacityChange}
        type="range"
        min="0"
        max="1"
        step="0.1"
        value="1"
    />100%
</label>
<div id="first" bind:this={firstb} />

<style>
    #first {
        width: 100px;
        height: 100px;
        background-color: black;
    }
</style>
