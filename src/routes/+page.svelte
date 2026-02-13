<svelte:head>
	<title>OpenPlan3D — Design Your Dream Space in 3D</title>
</svelte:head>

<!-- Hero -->
<section class="bg-gradient-to-b from-slate-900 via-slate-900 to-slate-800 text-white">
	<div class="max-w-6xl mx-auto px-6 py-24 md:py-32 text-center">
		<div class="inline-block bg-blue-500/10 text-blue-400 text-xs font-medium px-3 py-1 rounded-full mb-6 border border-blue-500/20">
			Free &amp; Open Source
		</div>
		<h1 class="text-4xl md:text-6xl font-bold tracking-tight leading-tight mb-6">
			Design Your Dream<br />Space in <span class="text-blue-500">3D</span>
		</h1>
		<p class="text-slate-400 text-lg md:text-xl max-w-2xl mx-auto mb-10 leading-relaxed">
			Draw floor plans in 2D, visualize in 3D, and furnish with 140+ models. 
			Export to PNG, SVG, DXF, PDF, and more. No signup required.
		</p>
		<div class="flex flex-col sm:flex-row gap-4 justify-center">
			<a
				href="https://app.openplan3d.com"
				class="bg-blue-500 hover:bg-blue-600 text-white font-semibold px-8 py-3.5 rounded-lg text-lg transition-colors shadow-lg shadow-blue-500/25"
			>
				Try Free Editor →
			</a>
			<a
				href="/features"
				class="border border-slate-600 hover:border-slate-500 text-slate-300 hover:text-white font-medium px-8 py-3.5 rounded-lg text-lg transition-colors"
			>
				See Features
			</a>
		</div>
	</div>
</section>

<!-- Editor Preview Mockup -->
<section class="bg-slate-800 py-16">
	<div class="max-w-5xl mx-auto px-6">
		<div class="bg-slate-900 rounded-xl border border-slate-700 overflow-hidden shadow-2xl">
			<div class="flex items-center gap-2 px-4 py-3 border-b border-slate-700">
				<div class="w-3 h-3 rounded-full bg-red-500/80"></div>
				<div class="w-3 h-3 rounded-full bg-yellow-500/80"></div>
				<div class="w-3 h-3 rounded-full bg-green-500/80"></div>
				<span class="text-slate-500 text-xs ml-2">app.openplan3d.com</span>
			</div>
			<div class="aspect-[16/9] bg-gradient-to-br from-slate-800 to-slate-900 flex items-center justify-center">
				<div class="text-center">
					<div class="text-6xl mb-4">🏠</div>
					<p class="text-slate-400 text-lg">Interactive 2D &amp; 3D Floor Plan Editor</p>
					<a href="https://app.openplan3d.com" class="inline-block mt-4 text-blue-400 hover:text-blue-300 text-sm font-medium transition-colors">
						Open in browser →
					</a>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Features Grid -->
<section class="bg-white py-20">
	<div class="max-w-6xl mx-auto px-6">
		<div class="text-center mb-16">
			<h2 class="text-3xl md:text-4xl font-bold text-slate-900 mb-4">Everything you need to plan your space</h2>
			<p class="text-slate-500 text-lg max-w-2xl mx-auto">Professional-grade tools, completely free. From quick sketches to detailed floor plans.</p>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
			{#each features as feature}
				<div class="group p-6 rounded-xl border border-slate-200 hover:border-blue-200 hover:shadow-lg transition-all">
					<div class="text-3xl mb-4">{feature.icon}</div>
					<h3 class="text-lg font-semibold text-slate-900 mb-2">{feature.title}</h3>
					<p class="text-slate-500 text-sm leading-relaxed">{feature.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- CTA -->
<section class="bg-slate-50 py-20">
	<div class="max-w-3xl mx-auto px-6 text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-slate-900 mb-4">Ready to design your space?</h2>
		<p class="text-slate-500 text-lg mb-8">Start creating beautiful floor plans in minutes. Free, no signup needed.</p>
		<a
			href="https://app.openplan3d.com"
			class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-semibold px-8 py-3.5 rounded-lg text-lg transition-colors shadow-lg shadow-blue-500/25"
		>
			Launch Editor →
		</a>
	</div>
</section>

<script>
	const features = [
		{ icon: '✏️', title: '2D Floor Plan Drawing', desc: 'Draw walls, rooms, doors, and windows with precise measurements. Snap-to-grid and orthogonal drawing modes.' },
		{ icon: '🧊', title: '3D Visualization', desc: 'Instantly switch to a 3D view of your floor plan. Walk through your design with orbit controls.' },
		{ icon: '🪑', title: '140+ Furniture Models', desc: 'Browse and place furniture from a curated library. Resize, rotate, and position items precisely.' },
		{ icon: '📱', title: 'RoomPlan / LiDAR Import', desc: 'Import room scans from Apple RoomPlan. Turn your real room into an editable floor plan.' },
		{ icon: '📐', title: 'Imperial & Metric Units', desc: 'Work in feet/inches or meters/centimeters. Switch anytime — measurements update automatically.' },
		{ icon: '📤', title: 'Export Anywhere', desc: 'Export to PNG, SVG, DXF, PDF, or JSON. Share your plans or continue editing in CAD software.' },
	];
</script>
