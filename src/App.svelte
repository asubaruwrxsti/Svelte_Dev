<script>
	var loggedIn = false;
	var username = '';

	if (!loggedIn) {
		username = 'guest';
	}

	var game_list = `
		{
			"games": [
				{
					"name": "Game 1",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 2",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 3",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 4",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 5",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 6",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 7",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 8",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				},
				{
					"name": "Game 9",
					"platform": "PC",
					"genre": "Action",
					"rating": 5,
					"status": "Playing"
				}
			]
		}
	`;

</script>
<style>
	h1 {
		position: absolute;
		top: 15px;
		left: 10px;
	}

	p {
		position: absolute;
		top: 95px;
		left: 10px;
	}

	.navbar {
		background-color: #e7d7d780;
		box-shadow: 0 0 10px #e7d7d780;
		backdrop-filter: blur(40px);
		z-index: 1;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
	}

	.navbar ul {
		display: flex;
		justify-content: space-around;
		align-items: center;
		list-style: none;
		margin: 0;
		padding: 0;
		height: 50px;
	}

	.navbar li {
		margin: 0;
		padding: 0;
		height: 100%;
		width: 25%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.navbar li:hover {
		background-color: #c4747480;
		box-shadow: 0 0 10px #c4747480;
		transition: 0.2s ease-in;
	}

	.navbar a {
		text-decoration: none;
		color: rgb(224, 224, 224);
		font-weight: bold;
		text-transform: uppercase;
	}

</style>
<nav class="navbar">
	<ul>
	  <li><a href="#">Home</a></li>
	  <li><a href="#">Library</a></li>
	  <li><a href="#">Utilities</a></li>
	  <li><a href="#">Account</a></li>
	</ul>
</nav>  

<h1>Hello {username}!</h1>
<p>These is the {username}'s game library.</p>