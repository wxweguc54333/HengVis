<script>
	import { base } from '$app/paths';
</script>

<svelte:head>
	<style>
		* {
			font-family: sans-serif;
		}

		body,
		html {
			margin: 0;
			padding: 0;
		}
	</style>
</svelte:head>

<div id="header">
	<h1>基于数据驱动断点的数据可视化</h1>
	<div class="staff" style="display: flex; justify-content: center; flex-direction: column; align-items: center; ">
		<p> Student: Heng Wang </p>
		<p> Supervisor: Benjamin Bach </p>
	</div>
</div>

<div>
	<div id="content">
		<slot />
	</div>
</div>

<div id="footer">
	<!-- <div id="di_logo">
		<img src="{base}/img/di_logo.png" alt="Svelte logo" style="width: auto; height=auto"/>
		<img src="{base}/img/edimg.png" alt="Svelte logo" style="width: auto; height=auto"/>
	</div> -->
</div>


<style>
	:global(body) {
		background-color: #F2F3F5;
	}
	h1 {
		font-size: 32px;
		font-weight: 400;
		margin: 0.4rem 0;
	}
	#header {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 0.7rem;
	}
	#content {
		padding: 0.7rem;
	}

	#footer {
		display: flex;
		justify-content: space-between;
		align-items: center;
		bottom: 0;
        right: 0;
		margin-left: 24px;
		margin-right: 24px;
		margin-bottom: 12px;
		margin-top: 36px;
	}

	#di_logo {
		display: inline-flex;
		height: 56px;
		justify-content: center;
		gap: 16px;
	}
</style>