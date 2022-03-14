<p>Lets try this again huh?</p>
<script>
	let count = 0;

	$: if (count === 10) {
		alert(`COME ON!`);
	
	}
    $: if (count === 15) {
        alert(`SHOW ME WHAT YOU GOT!`)
    }
    $: if (count === 20) {
        alert(`ALMOST THERE!`)
    }
    $: if (count === 25) {
        alert(`You win!.... Nothing.. TADAAAA`)
    }

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>