<script>

    import Login from './Login.svelte';

	var loggedIn = false;
	var username = 'Arlind';

	if (!loggedIn) {
		username = 'guest';
	}
	
	import 'bootstrap/dist/css/bootstrap.min.css';
	import 'bootstrap/dist/js/bootstrap.min.js';
</script>
<style>
	.offcanvas {
		background-image: url('https://source.unsplash.com/1600x900/?nature,water');
	}

	.offcanvas-header {
		color : #fff;
		background-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
	}

	.offcanvas-body {
		background-image : linear-gradient(to bottom, rgba(0,0,0,0), rgba(0,0,0,1));
	}

	.border-0 {
		background-color : hwb(0 100% 0% / 0.452);
		/* add blur */
		backdrop-filter: blur(10px);
	}
</style>
<nav class="navbar bg-body-tertiary fixed-top">
	<div class="container-fluid">
	  <a class="navbar-brand" href="#">Hello {username.toUpperCase()}!</a>
	  <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
		<span class="navbar-toggler-icon"></span>
	  </button>
	  <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
		<div class="offcanvas-header">
		  <h5 class="offcanvas-title" id="offcanvasNavbarLabel">{username.toUpperCase()}</h5>
		  <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
		</div>
		<div class="offcanvas-body">
			<div class="border-0 rounded">
				<ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
					{#if loggedIn}
						<li class="nav-item">
							<a class="nav-link active" aria-current="page" href="#">Home</a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#">Library</a>
						</li>
						<li class="nav-item dropdown">
							<a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
								Account
							</a>
							<ul class="dropdown-menu">
								<li><a class="dropdown-item" href="#">Settings</a></li>
								<li><a class="dropdown-item" href="#">Utilities</a></li>
								<li><a class="dropdown-item" href="#">Logout</a></li>
							</ul>
						</li>
					{:else}
						<Login />
					{/if}
				</ul>
			</div>
		</div>
	  </div>
	</div>
  </nav>