<script>
	let sayit = Math.random() < 0.5 ? 'duh' : 'noduh';

	$: {
		sayit;
	}
</script>

<div>
	{sayit}
</div>

<style>
	div {
		font-size: 5rem;
		text-align: center;
		padding-top: 2.5rem;
	}
</style>
