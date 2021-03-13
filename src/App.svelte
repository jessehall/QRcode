<script>
	import QrCode from "svelte-qrcode";
	let domain = "https://google.com";
	let name = 'jesse';
	let myDomain = "";
	function handleSubmit(e) {
		
		myDomain = e;
		console.log(myDomain);
		
	}

</script>



<main>
	<div class="container">
		<h1>
			Dynamically Generate a QR code:
		</h1>
		<p>Type in a URL and hit enter to generat a QR code:</p>
		<input bind:value={domain} size="50"><button on:click={handleSubmit(domain)}>Create QR code</button><br>
		{#if myDomain}
	  		<QrCode value={myDomain} />
			  
	  	{/if}
	  
	</div>

	<!-- <input bind:value={domain}> -->
	<h1>Domain: {domain}</h1>
</main>

<style>
	
</style>