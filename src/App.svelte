<script>
	import C from 'js-ktc';

	let ktc = new C('secret');
	let messageToEncrypt = '';
	let messageToDecrypt = '';
	let encryptedMessage = '';
	let decryptedMessage = '';

	function encrypt() {
		encryptedMessage = ktc.encrypt(messageToEncrypt);
	}

	function decrypt() {
		decryptedMessage = ktc.decrypt(messageToDecrypt);
	}
</script>

<main>
	<div class="container">
	<div class="row">
		<div class="col-lg-6 col-md-12">
		<div class="card mt-4 shadow-lg">
			<div class="card-header bg-primary text-white">
			<h3>Cifrar</h3>
			</div>
			<div class="card-body">
			<textarea class="form-control" rows="4" bind:value={messageToEncrypt}></textarea>
			<button class="btn btn-outline-primary mt-2" on:click={encrypt}>Cifrar</button>
			<textarea class="form-control mt-2" rows="4" bind:value={encryptedMessage} readonly></textarea>
			</div>
		</div>
		</div>
		<div class="col-lg-6 col-md-12">
		<div class="card mt-4 shadow-lg">
			<div class="card-header bg-warning text-white">
			<h3>Descifrar</h3>
			</div>
			<div class="card-body">
			<textarea class="form-control" rows="4" bind:value={messageToDecrypt}></textarea>
			<button class="btn btn-outline-warning mt-2" on:click={decrypt}>Descifrar</button>
			<textarea class="form-control mt-2" rows="4" bind:value={decryptedMessage} readonly></textarea>
			</div>
		</div>
		</div>
	</div>
	</div>
</main>

<style>
  /* Estilos de colores */
  .container {
    background-color: #f0f0f0;
  }

  .text-primary {
    color: #007bff;
  }

  .text-warning {
    color: #ffc107;
  }

  .btn-primary {
    background-color: #007bff;
    border-color: #007bff;
  }

  .btn-primary:hover {
    background-color: #0056b3;
    border-color: #0056b3;
  }

  .btn-warning {
    background-color: #ffc107;
    border-color: #ffc107;
  }

  .btn-warning:hover {
    background-color: #d8a000;
    border-color: #d8a000;
  }
</style>