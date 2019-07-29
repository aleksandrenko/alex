<script>
	export let segment;

	const onBackClick = () => {
		window.history.back();
	}
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
		padding: 10px;
	}
</style>

<nav>
	<ul>
		<li on:click={onBackClick}>Back</li>
		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <li><a rel=prefetch class='{segment === "blog" ? "selected" : ""}' href='blog'>blog</a></li> -->
		<li><a href='./documents/'>Documents</a></li>
		<li><a href='./profile/'>Profile</a></li>
		<li><a href='./about/'>About</a></li>
		<li><a href='./logout/'>Logout</a></li>
	</ul>
</nav>