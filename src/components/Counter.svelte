<script>
    
    export let value = 0;
    
    const increaseValue = () => {
        value++;
    };
    const decreaseValue = () => {
        value--;
    };
    const resetValue = () => {
        value = 0;
    };
</script>

<div class="counter">
    <h2>{value}</h2>
    <div class="buttons">
        <button on:click={decreaseValue} class="less"> - </button>  
        <button on:click={resetValue}> reset </button>
        <button on:click={increaseValue} class="more"> + </button>
    </div>
</div>

<style>
    .counter {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 300px;
        height: 200px;
        background-color: black;
        border-radius: 5px;
        box-shadow: 1px 3px 5px #000000;
        border: 6px solid gray;
    }
    h2 {
        background-color: black;
        color: red;
        font-size: 6rem;
        padding: 0;
        margin: 0;
        font-weight: 100;
        text-transform: uppercase;
    }
    button {
        margin: none;
        border: none;
        border-radius: 0;
        border: 1px solid grey;
        width: 100%;
        padding: 0.6rem 1rem;
        font-size: 1.2rem;
        font-weight: 600;
        cursor: pointer;
    }
    .buttons {
        display: flex;
    }
    .less {
        border-radius: 6px 0 0 6px;
    }
    .more {
        border-radius: 0 6px 6px 0;
    }
</style>