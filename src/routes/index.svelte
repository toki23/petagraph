<script>
	import '@carbon/charts/styles.min.css';
	import 'carbon-components/css/carbon-components.min.css';

	import parseTextTodata from '$lib/utils/parseTextToData';
	import { LineChart } from '@carbon/charts-svelte';

	let data = '';
	const inputeData = () => {
		console.log(parseTextTodata(data));
	};
</script>

<h1>input data here</h1>
<textarea bind:value={data} on:input={inputeData} />

<LineChart
	data={[
		{ group: 1, key: 1, value: 1 },
		{ group: 1, key: 2, value: 4 },
		{ group: 1, key: 3, value: 9 },
		{ group: 1, key: 4, value: 16 },
		{ group: 1, key: 5, value: 25 }
	]}
	options={{
		title: 'Line (discrete)',
		axes: {
			bottom: {
				title: '2019 Annual Sales Figures',
				mapsTo: 'key',
				scaleType: 'labels'
			},
			left: {
				mapsTo: 'value',
				title: 'Conversion rate',
				scaleType: 'linear'
			}
		},
		height: '400px'
	}}
/>

<!-- graph Data
1	2
2	4
3	8
4	16



\-->
