<script lang="ts">
    import { inputValue, operation, previousValue } from "./store";
    const handleClick = () => {
        let currentValue;
        inputValue.subscribe(x => currentValue = x);
        let prevValue;
        previousValue.subscribe(x => prevValue = x);
        let currentOp;
        operation.subscribe(x => currentOp = x);
        let calculatedValue: number;
        switch(currentOp) {
            case '+':
                calculatedValue = Number.parseFloat(currentValue) + Number.parseFloat(prevValue);
                break;
            case '-':
                calculatedValue = Number.parseFloat(prevValue) - Number.parseFloat(currentValue);
                break;
            case '*':
                calculatedValue = Number.parseFloat(prevValue) * Number.parseFloat(currentValue);
                break;
            case '/':
                calculatedValue = Number.parseFloat(prevValue) / Number.parseFloat(currentValue);
                break;
        }
        inputValue.set(calculatedValue.toString());
    }
</script>

<div class="col-6 calc-btn" on:click={handleClick}>
    <div class="wrapper"> = </div>
</div>