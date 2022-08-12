<script lang="ts">
    import { inputValue } from './store';
    const handleClick = () => {
        inputValue.update(num => {
            return `${num}.`
        })
    }
</script>

<div class="col-3 calc-btn" on:click={handleClick} > 
    <div class="wrapper">.</div>
</div>