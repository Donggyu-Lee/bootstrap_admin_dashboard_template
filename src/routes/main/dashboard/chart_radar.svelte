<script>
	import { onMount } from 'svelte';

	var optionsRadar = {
		colors: ['var(--bs-border-color)', 'var(--bs-primary)'],
		series: [
			{
				name: 'Visitors',
				data: [180, 150, 130, 140, 205, 140]
			},
			{
				name: 'Unique visitors',
				data: [78, 102, 69, 58, 132, 98]
			}
		],
		chart: {
			height: 240,
			type: 'radar',
			fontFamily: 'inherit',
			dropShadow: {
				enabled: true,
				blur: 12,
				left: 0,
				top: 4,
				opacity: 0.05
			},
			toolbar: {
				show: false
			}
		},
		stroke: {
			width: 0
		},
		fill: {
			opacity: 1
		},
		markers: {
			size: 0
		},
		xaxis: {
			strokeWidth: 0,
			categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
		},
		yaxis: {
			show: false
		},
		plotOptions: {
			radar: {
				polygons: {
					strokeWidth: 0
				}
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chart_radar'), optionsRadar);
		chart.render();
	});
</script>

<div class="col-12 col-md-6 mb-3 mb-lg-5">
	<div class="card">
		<div class="card-header">
			<h5 class="mb-0">Chart Radar</h5>
		</div>
		<!--Chart-->
		<div id="chart_radar" />
	</div>
</div>
