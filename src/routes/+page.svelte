<script>
	import Insta from '$lib/Insta.svelte';
	import Linkedin from '$lib/Linkedin.svelte';
	import Facebook from '../lib/Facebook.svelte';
	import Spotify from '../lib/Spotify.svelte';
</script>

<h1>My profile card</h1>
<p>Welcome to my profile card</p>

<!-- <div class="grid-container">
	<div class="grid-item">1</div>
	<div class="grid-item">3</div>
	<div class="grid-item">4</div>
	<div class="grid-item">5</div>
	<div class="grid-item">6</div>
	<div class="grid-item">7</div>
</div> -->

<div class="wrapper">
	<div class="box1 all-boxes"></div>
	<div class="box2 all-boxes">
		<div class="contact-info">
			<p>Contact me</p>
			<div class="links">
				<a href="https://www.instagram.com/ellenoor_bok/"><Insta /></a>
				<a href="https://www.linkedin.com/in/ellenoor-bok-029096290/"><Linkedin /></a>
				<a href="https://www.facebook.com/ellenoor.bok?locale=nl_NL"><Facebook /></a>
			</div>
		</div>
	</div>
	<div class="box3 all-boxes">
		<p>My playlist</p>
		<a href="https://open.spotify.com/playlist/6kmyiZ6DMKM7XhXY12fDlp?si=104890592cb74da5"
			><Spotify /></a
		>
	</div>
	<div class="box4 all-boxes">
		<p class="iam">IAM Core</p>
	</div>
	<div class="box5 all-boxes">Five</div>
</div>

<style>
	* {
		transition: 0.5s;
		overflow-y: scroll;
	}

	h1,
	p {
		display: flex;
		color: white;
		justify-content: center;
		align-items: center;
	}

	div,
	div p {
		color: black;
	}

	.contact-info {
		display: flex;
		flex-direction: column;
		align-items: center;
		font-size: 20px;
	}

	a {
		margin: 10px;
		color: black;
	}

	.all-boxes a {
		display: inline-block;
		margin: 0 10px;
	}

	.all-boxes a:hover {
		color: #f774c4;
		transform: scale(1.5);
		transition: font-size 0.5s;
	}

	.all-boxes {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		height: 100%;
		margin: 10px;
		justify-content: center;
		align-items: center;
		border-radius: 10px;
	}

	.wrapper {
		display: grid;
		grid-template-columns: 1fr 1fr; /* 2 columns */
		grid-auto-rows: 100px;
		row-gap: 1em;
        overflow-y: scroll;
	}

	.box1 {
		background-color: #f774c4;
		position: relative;
		height: 300px;
		object-fit: fill;
		border: #f774c4 solid 15px;
		grid-column-start: 1;
		grid-column-end: 3;
		grid-row-start: 1;
		grid-row-end: 4;
	}

	.box1::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-size: cover;
		background-image: url(./images/fotoVerticaal.JPG);
		border-radius: 10px;
	}

	.box2 {
		background-color: #f1ff47;
		width: 50vw;
		grid-column-start: 1;
		grid-row-start: 4;
		grid-row-end: 5;
	}

	.box3 {
		background-color: #14d761;
		grid-column-start: 2;
		grid-row-start: 4;
		grid-row-end: 5;
	}

	.box4 {
		position: relative;
		height: 210px;
		object-fit: fill;
		background-color: #6a00ba;
		border: #6a00ba solid 15px;
		grid-column-start: 1;
		grid-column-end: 3;
		grid-row-start: 5;
		grid-row-end: 6;
        z-index: -2;
	}

	.box4::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-size: cover;
		background-image: url(./images/groepsfotoIAM.JPG);
		border-radius: 10px;
        z-index: -1;
	}

    .iam{
        z-index: 1;
        font-size: 30px;
        justify-content: center;
        align-items: center;
        color: #f774c4;
    }

	.box5 {
		background-color: #ff8b1e;
		grid-column-start: 1;
		grid-column-end: 3;
		grid-row-start: 6;
		grid-row-end: 7;
        z-index: -5;
	}

	@media only screen and (min-width: 475px) {
		.all-boxes {
			display: grid;
			height: 100%;
			margin: 0.5em;
			justify-content: center;
			align-items: center;
		}

		.wrapper {
			display: grid;
			grid-template-columns: repeat(3, 1fr);
			grid-auto-rows: 100px;
			column-gap: 1em;
			row-gap: 1em;
		}

		.box1 {
			grid-column-start: 1;
			grid-column-end: 4;
			grid-row-start: 1;
			grid-row-end: 3;
		}

		.box2 {
			grid-column-start: 1;
			grid-row-start: 3;
			grid-row-end: 5;
		}
	}

	@media only screen and (min-width: 475px) and (max-width: 800px) {
		.all-boxes {
			display: grid;
			height: 100%;
			margin: 0.5em;
			justify-content: center;
			align-items: center;
		}

		.wrapper {
			display: grid;
			grid-template-columns: repeat(2, 1fr);
			grid-auto-rows: 100px;
			column-gap: 1em;
			row-gap: 1em;
		}

		.box1 {
			grid-column-start: 1;
			grid-column-end: 2;
			grid-row-start: 1;
			grid-row-end: 3;
		}

		.box2 {
			grid-column-start: 1;
			grid-row-start: 3;
			grid-row-end: 5;
		}
	}

	@media only screen and (min-width: 800px) and (max-width: 1200px) {
		.all-boxes {
			display: grid;
			height: 100%;
			margin: 0.5em;
			justify-content: center;
			align-items: center;
		}

		.wrapper {
			display: grid;
			grid-template-columns: repeat(3, 1fr);
			grid-auto-rows: 100px;
			column-gap: 1em;
			row-gap: 1em;
		}

		.box1 {
			grid-column-start: 1;
			grid-column-end: 2;
			grid-row-start: 1;
			grid-row-end: 3;
		}

		.box2 {
			grid-column-start: 1;
			grid-row-start: 3;
			grid-row-end: 5;
		}
	}

	@media only screen and (min-width: 1200px) {
		.all-boxes {
			display: grid;
			height: 100%;
			margin: 0.5em;
			justify-content: center;
			align-items: center;
		}

		.wrapper {
			display: grid;
			grid-template-columns: repeat(4, 1fr);
			grid-auto-rows: 100px;
			column-gap: 1em;
			row-gap: 1em;
		}

		.box1 {
			grid-column-start: 1;
			grid-column-end: 2;
			grid-row-start: 1;
			grid-row-end: 3;
		}

		.box2 {
			grid-column-start: 1;
			grid-row-start: 3;
			grid-row-end: 5;
		}
	}
</style>
