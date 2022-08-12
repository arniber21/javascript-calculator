<script lang="ts">
import { inputValue } from "./store";


    export let value: number;

    const handleClick = () => {
        inputValue.update(num => {
            return `${num}${value.toString()}`
        })
    }
</script>

<div class="col-3 calc-btn" on:click={handleClick} >
    <div class="wrapper"> { value.toString() }</div>
</div>