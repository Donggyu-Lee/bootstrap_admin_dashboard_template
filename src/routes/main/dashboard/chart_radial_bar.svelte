<script>
	import { onMount } from 'svelte';
	var optionsRadialBar = {
		colors: ['var(--bs-primary)'],
		series: [76],
		chart: {
			type: 'radialBar',
			offsetY: 0,
			fontFamily: 'inherit',
			height: 400,
			sparkline: {
				enabled: true
			}
		},
		plotOptions: {
			radialBar: {
				startAngle: -90,
				endAngle: 90,
				track: {
					opacity: 0.2,
					background: 'var(--bs-primary)',
					strokeWidth: '100%',
					margin: 5, // margin is in pixels
					dropShadow: {
						enabled: true,
						top: 2,
						left: 0,
						color: '#000',
						opacity: 0.1,
						blur: 12
					}
				},
				dataLabels: {
					name: {
						show: true,
						offsetY: -30,
						fontSize: '14px',
						fontWeight: '400'
					},
					value: {
						offsetY: -20,
						fontSize: '20px',
						fontWeight: '700',
						color: 'currentColor'
					}
				}
			}
		},
		fill: {
			opacity: 1
		},
		grid: {
			padding: {
				top: -30,
				bottom: 50
			}
		},
		labels: ['Conversion Rate']
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chart_radial_bar'), optionsRadialBar);
		chart.render();
	});
</script>

<div class="col-12 col-md-6 mb-3 mb-lg-5">
	<div class="card overflow-hidden">
		<div class="card-header">
			<h5 class="mb-0">Chart Radial Bar</h5>
		</div>
		<!--Chart-->
		<div id="chart_radial_bar" />
	</div>
</div>
