<script>
	import Chart from '$lib/components/chart.svelte'
	import parseTextTodata from '$lib/utils/parseTextToData';

	let data = '';
	const inputeData = () => {
		console.log(parseTextTodata(data));
	};
</script>

<h1>input data here</h1>
<textarea bind:value={data} on:input={inputeData} />
<Chart></Chart>

<!-- graph Data
1	2
2	4
3	8
4	16



\-->
