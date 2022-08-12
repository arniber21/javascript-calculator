<script lang="ts">
	import svelteLogo from "./assets/svelte.svg";
import CalculatorDecimalButton from "./lib/CalculatorDecimalButton.svelte";
import CalculatorEquals from "./lib/CalculatorEquals.svelte";
import CalculatorInput from "./lib/CalculatorInput.svelte";
import CalculatorNumber from "./lib/CalculatorNumber.svelte";
import CalculatorOperation from "./lib/CalculatorOperation.svelte";
</script>

<div class="container text-center p-3">
	<h1>JavaScript Calculator</h1>
	<div class="row">
		<CalculatorInput />
		<CalculatorNumber value={1}/>
		<CalculatorNumber value={2}/>
		<CalculatorNumber value={3}/>
		<CalculatorOperation op='+' />
		<CalculatorNumber value={4}/>
		<CalculatorNumber value={5}/>
		<CalculatorNumber value={6}/>
		<CalculatorOperation op='-' />
		<CalculatorNumber value={7}/>
		<CalculatorNumber value={8}/>
		<CalculatorNumber value={9}/>
		<CalculatorOperation op='*' />
		<CalculatorEquals />
		<CalculatorDecimalButton />
		<CalculatorOperation op='/' />
	</div>
</div>
