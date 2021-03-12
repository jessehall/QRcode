<script>
	import QrCode from "svelte-qrcode";
	let domain = "https://www.swervecreative.com";
</script>



<main>
	<div class="container">
		<h1>
			Dynamically Generate a QR code:
		</h1>
		<p>Type in a URL and hit enter to generat a QR code:</p>
		<input value={domain} size="50"><br>
	  <QrCode value={domain} />
	</div>
</main>

<style>
	
</style>