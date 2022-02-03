<script>
	import '@carbon/charts/styles.min.css';
	import 'carbon-components/css/carbon-components.min.css';
	import { LineChart } from '@carbon/charts-svelte';
</script>
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
