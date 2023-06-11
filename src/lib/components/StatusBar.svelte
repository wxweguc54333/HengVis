<script>
	export let width, height;
	export let landscapeOverlay;
	export let viewLandscape;
	import "carbon-components-svelte/css/white.css";
	import { Checkbox } from "carbon-components-svelte";

	$: width;
	$: height;

	let divAR, divArea;

	$: divAR = Math.round((width / height) * 100) / 100;
	$: divArea = Math.round(width * height);
</script>

<div id="controls">
	<p>
		使用右下角的手柄调整容器的大小，并观察可视化的更新 (Chrome/Firefox only).
	</p>

	<ul>	
		<li>宽度: {width} px</li>
		<li>高度: {height} px</li>
		<li>纵横比: {divAR}</li>
		<li>面积: {divArea} px</li>
		<li />
	</ul>

	<p>
		<Checkbox labelText="展示由断点划分的区域" bind:checked={landscapeOverlay} id="overlay"/>
	</p>
</div>

<style>
	#controls {
		/* line-height: 1rem; */
		margin-bottom: 0.3rem;
	}
	p,
	ul {
		margin: 0;
		line-height: 1.3rem;
		font-weight: 400;
	}
	input {
		margin: 0 5px 7px 0;
	}
	ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
		display: inline-block;
	}
	li {
		display: inline-block;
		width: 150px;
	}
	button {
		background-color: white;
		color: black;
		border: 2px solid #bebada;
		border-radius: 2rem;
		padding: 0.25rem 0.5rem 0.15rem 0.5rem;
		font-size: 0.8rem;
		transition-duration: 0.3s;
	}
	button:hover {
		background-color: #bebada;
	}
</style>
