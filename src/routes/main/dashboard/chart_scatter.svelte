<script>
	import { onMount } from 'svelte';

	var optionsScatter = {
		colors: ['var(--bs-primary)', 'var(--bs-danger)', 'var(--bs-info)', 'var(--bs-warning)'],
		series: [
			{
				name: 'Sent',
				data: [30, 40, 50, 60, 24, 20, 15]
			},
			{
				name: 'Received',
				data: [7, 12, 14, 17, 10, 13, 8]
			}
		],
		chart: {
			height: 350,
			type: 'scatter',
			fontFamily: 'inherit',
			zoom: {
				enabled: false
			},
			toolbar: {
				show: false
			}
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: {
				// @ts-ignore
				formatter: function (val) {
					return val + ' <span class="fw-normal text-body-secondary">Emails</span>';
				}
			}
		},
		dataLabels: {
			enabled: false
		},
		fill: {
			opacity: 1
		},
		labels: ['Mon', 'Tue', 'Wed', 'Thr', 'Fri', 'Sat', 'Sun'],
		xaxis: {
			type: 'category',
			axisTicks: {
				show: true
			},
			axisBorder: {
				show: false
			},

			crosshairs: {
				show: true,
				stroke: {
					width: 2,
					dashArray: 0
				}
			}
		},
		yaxis: {
			max: 70,
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			},

			labels: {
				offsetX: 6
			}
		},
		grid: {
			strokeDashArray: 4,
			padding: {
				left: 24,
				bottom: 20,
				right: 30
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chart_scatter'), optionsScatter);
		chart.render();
	});
</script>

<div class="col-12 mb-3 mb-lg-5">
	<div class="card">
		<div class="card-header">
			<h5 class="mb-0">Chart Scatter</h5>
		</div>
		<!--Chart-->
		<div id="chart_scatter" />
	</div>
</div>
