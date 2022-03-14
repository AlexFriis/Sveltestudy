<script>
	import Hello from './Intro/Hello.svelte';
	import Styled from './Intro/Styled.svelte';
	import Htmlstring from './Intro/Htmlstring.svelte';
	import Clickme from './Reactivity/Clickme.svelte';
	import Clickmeagain from './Reactivity/Clickmeagain.svelte';
	import Firstprop from './Props/Firstprop.svelte';
	import Secondprop from './Props/Secondprop.svelte';
	import Firstevent from './Events/Firstevent.svelte';
	
	export let menu = 1;

	const proppkg = {
		model: 'Porsche 718 Spyder',
		horsepower: '420',
		topspeed: '301 km/h'
	}
</script>

<p>Use the menu below to jump into something else!</p>

<ul id="menu">
	<li><a href="/" on:click|preventDefault={() => (menu = 1)}>Hello!</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 2)}>Style?</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 3)}>HTML?</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 4)}>Click me?</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 5)}>Click me again?</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 6)}>First prop</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 7)}>Second prop</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 8)}>Tracking?</a></li> |
</ul>


{#if menu === 1}
<Hello/>
{:else if menu === 2}
<Styled/>
{:else if menu === 3}
<Htmlstring/>
{:else if menu === 4}
<Clickme/>
{:else if menu === 5}
<Clickmeagain/>
{:else if menu === 6}
<Firstprop answer={'not the droids you are looking for'}/>
{:else if menu === 7}
<Secondprop {...proppkg}/>
{:else if menu === 8}
<Firstevent/>

{/if}

<p> bla bla bla fix git please</p>
<p> bla bla bla fix git please</p>
<p> bla bla bla fix git please</p>
<p> bla bla bla fix git please</p>
<style>

	ul#menu li {
		display : inline;
	}	

</style>