<!-- +page.svelte -->
<script>
	import SpaceBackground from '../lib/SpaceBackground.svelte';

	function clickMail() {
		const a = "aGlAbWlrYS"
		const b = atob(a + "1wZXRhay5kZQ==");
		window.location.href = `mailto:${b}`;
	}
</script>

<svelte:head>
	<title>Mika Petak - Portfolio</title>
	<meta name="description" content="Cybersecurity Student Portfolio" />
</svelte:head>

<!-- Space Background Component -->
<SpaceBackground />

<!-- Main Content -->
<div class="min-h-screen flex items-center justify-center p-8 relative z-10">
	<div class="bg-white/5 backdrop-blur-3xl border border-white/10 rounded-3xl p-12 text-center max-w-lg w-full shadow-2xl transform transition-all duration-300 hover:shadow-4xl hover:shadow-purple-500/20">

		<!-- Profile Section -->
		<div class="mb-8">
			<div class="w-32 h-32 bg-gradient-to-br from-purple-400 via-pink-400 to-blue-400 rounded-full mx-auto mb-6 flex items-center justify-center text-4xl font-bold border-4 border-white/20 shadow-lg shadow-purple-500/30">
				MP
			</div>
			<h1 class="text-5xl font-bold mb-2 gradient-text">
				Mika Petak
			</h1>
			<p class="text-xl text-white/70 mb-8">
				Cybersecurity Student and Web Development Enthusiast.
			</p>
		</div>

		<!-- Links Section -->
		<div class="flex flex-col sm:flex-row gap-4 justify-center">
			<a href="https://github.com/mikap0703"
				 target="_blank"
				 class="inline-flex items-center gap-3 px-6 py-3 bg-white/10 border border-white/20 rounded-xl text-white font-medium transition-all duration-300 hover:bg-white/20 hover:shadow-lg hover:shadow-blue-500/30 backdrop-blur-xl">
				<svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor">
					<path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
				</svg>
				GitHub
			</a>

			<a href="https://www.linkedin.com/in/mika-petak-8b7a34246"
				 target="_blank"
				 class="inline-flex items-center gap-3 px-6 py-3 bg-white/10 border border-white/20 rounded-xl text-white font-medium transition-all duration-300 hover:bg-white/20 hover:shadow-lg hover:shadow-blue-500/30 backdrop-blur-xl">
				<svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor">
					<path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
				</svg>
				LinkedIn
			</a>

			<button
				onclick={clickMail}
				 class="inline-flex items-center gap-3 px-6 py-3 bg-white/10 border border-white/20 rounded-xl text-white font-medium transition-all duration-300 hover:bg-white/20 hover:shadow-lg hover:shadow-purple-500/30 backdrop-blur-xl">
				<svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor">
					<path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-.904.732-1.636 1.636-1.636h1.82L12 11.64l8.545-7.819h1.82c.904 0 1.636.732 1.636 1.636z"/>
				</svg>
				Email
			</button>
		</div>
	</div>
</div>

<style>
    :global(.gradient-text) {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }
</style>