<script>
	let answer = '';
	let sayit = '';

	function duhOrNoDuh() {
		answer = Math.random() < 0.5 ? 'duh' : 'no duh';
	}
	$: {
		answer;
		sayit;
	}
</script>

<div class="everything">
	<input bind:value={sayit} type="text" id="sayit" size="20" placeholder="Say it" />
	<button disabled={!sayit} on:click={duhOrNoDuh}>Should I say duh or no duh</button>
	{#if answer && sayit}
		<div class="answer">
			<div class="you">'{sayit}'</div>
			<div class="me">'{answer}'</div>
		</div>
	{/if}
</div>

<style>
	* {
		font-family: 'Times New Roman', Times, serif;
		font-weight: bold;
	}

	.you {
		font-weight: normal;
	}

	.me {
		padding-top: 1vh;
	}

	.answer {
		padding: 1vh;
		font-size: 1.5em;
		position: absolute;
	}

	.everything {
		padding: 1vh;
	}

	input {
		font-size: 1.5em;
		font-weight: normal;
	}

	button {
		height: 3vh;
		width: 100px;
		margin-left: 1vw;
		position: absolute;
		font-weight: normal;
	}
</style>
