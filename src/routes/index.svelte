<script>
	let data = '';
	const inputeData = () => {
		console.log(data);
	};
</script>

<h1>input data here</h1>
<textarea bind:value={data} on:input={inputeData} />
<!-- graph Data
1	2
2	4
3	8
4	16



\-->