<script lang="ts">
    export let op: string;
    import { inputValue, operation, previousValue } from './store';

    const handleClick = () => {
        operation.set(op);
        previousValue.update(val => {
            let retVal: string;
            inputValue.subscribe(x => {
                retVal = x;
            })
            return retVal;
        });
        inputValue.set("");
    }
</script>

<div class="col-3 calc-btn" on:click={handleClick} >
    <div class="wrapper"> { op } </div>
</div>