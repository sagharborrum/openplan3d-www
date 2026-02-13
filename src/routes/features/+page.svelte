<svelte:head>
	<title>Features — OpenPlan3D</title>
	<meta name="description" content="Explore OpenPlan3D's powerful features: 2D/3D floor plan editing, 140+ furniture models, multi-format export, RoomPlan import, and more." />
</svelte:head>

<section class="bg-gradient-to-b from-slate-900 to-slate-800 text-white py-20">
	<div class="max-w-4xl mx-auto px-6 text-center">
		<h1 class="text-4xl md:text-5xl font-bold tracking-tight mb-6">Powerful features,<br /><span class="text-blue-500">zero cost</span></h1>
		<p class="text-slate-400 text-lg max-w-2xl mx-auto">Everything you need to design, visualize, and share professional floor plans — all in your browser.</p>
	</div>
</section>

<section class="bg-white py-20">
	<div class="max-w-4xl mx-auto px-6 space-y-20">
		{#each featureGroups as group}
			<div class="grid md:grid-cols-2 gap-12 items-start">
				<div>
					<div class="text-4xl mb-4">{group.icon}</div>
					<h2 class="text-2xl font-bold text-slate-900 mb-3">{group.title}</h2>
					<p class="text-slate-500 leading-relaxed mb-4">{group.desc}</p>
					<ul class="space-y-2">
						{#each group.bullets as bullet}
							<li class="flex items-start gap-2 text-sm text-slate-600">
								<span class="text-blue-500 mt-0.5">✓</span>
								<span>{bullet}</span>
							</li>
						{/each}
					</ul>
				</div>
				<div class="bg-slate-50 rounded-xl border border-slate-200 aspect-[4/3] flex items-center justify-center">
					<span class="text-6xl">{group.icon}</span>
				</div>
			</div>
		{/each}
	</div>
</section>

<!-- CTA -->
<section class="bg-slate-50 py-20">
	<div class="max-w-3xl mx-auto px-6 text-center">
		<h2 class="text-3xl font-bold text-slate-900 mb-4">See it in action</h2>
		<p class="text-slate-500 text-lg mb-8">Try every feature for free — no account required.</p>
		<a
			href="https://app.openplan3d.com"
			class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-semibold px-8 py-3.5 rounded-lg text-lg transition-colors shadow-lg shadow-blue-500/25"
		>
			Open Free Editor →
		</a>
	</div>
</section>

<script>
	const featureGroups = [
		{
			icon: '✏️',
			title: '2D Floor Plan Drawing',
			desc: 'Draw precise floor plans with an intuitive click-and-drag interface. Create complex multi-room layouts in minutes.',
			bullets: [
				'Click to place walls with automatic corner snapping',
				'Add doors and windows with configurable sizes',
				'Orthogonal and freeform drawing modes',
				'Undo/redo with full history',
				'Snap-to-grid for pixel-perfect layouts',
			]
		},
		{
			icon: '🧊',
			title: '3D Visualization',
			desc: 'See your floor plan come to life in a real-time 3D view. Navigate your design with intuitive orbit controls.',
			bullets: [
				'Instant 2D to 3D conversion',
				'Orbit, pan, and zoom camera controls',
				'Real photo-realistic wall and floor textures',
				'Dynamic lighting and shadows',
				'Toggle between 2D and 3D with one click',
			]
		},
		{
			icon: '🪑',
			title: '140+ Furniture Models',
			desc: 'Furnish your space with a growing library of 3D furniture models organized by room type.',
			bullets: [
				'Living room, bedroom, kitchen, bathroom, office furniture',
				'Drag and drop placement',
				'Resize and rotate freely',
				'Accurate real-world dimensions',
				'Models render in both 2D and 3D views',
			]
		},
		{
			icon: '📱',
			title: 'RoomPlan & LiDAR Import',
			desc: 'Scan your real room with Apple RoomPlan on iPhone or iPad and import the result directly into the editor.',
			bullets: [
				'Import RoomPlan JSON files',
				'Automatic wall, door, and window detection',
				'Edit scanned rooms like any other plan',
				'LiDAR-powered precision from your phone',
			]
		},
		{
			icon: '📐',
			title: 'Imperial & Metric Units',
			desc: 'Work in the measurement system you prefer. All dimensions update in real-time when switching.',
			bullets: [
				'Feet/inches and meters/centimeters',
				'Live dimension labels on walls',
				'Switch units at any time',
				'Consistent precision across formats',
			]
		},
		{
			icon: '📤',
			title: 'Multi-Format Export',
			desc: 'Export your plans in the format you need — for printing, sharing, or further editing in CAD tools.',
			bullets: [
				'PNG — high-resolution raster images',
				'SVG — scalable vector graphics',
				'DXF — AutoCAD-compatible format',
				'PDF — print-ready documents',
				'JSON — full plan data for backup or sharing',
			]
		},
		{
			icon: '🏢',
			title: 'Multi-Floor Support',
			desc: 'Design multi-story buildings with independent floor plans that share a common footprint.',
			bullets: [
				'Add and manage multiple floors',
				'Copy floor layouts between levels',
				'Switch floors instantly',
			]
		},
		{
			icon: '🎨',
			title: 'Real Photo Textures',
			desc: 'Apply realistic materials to walls, floors, and surfaces. Choose from wood, tile, carpet, concrete, and more.',
			bullets: [
				'Curated texture library',
				'Apply per-room or per-surface',
				'Realistic rendering in 3D view',
			]
		},
	];
</script>
