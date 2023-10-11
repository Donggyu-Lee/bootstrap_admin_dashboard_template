<script>
	import { onMount } from 'svelte';

	// @ts-ignore
	var optionsLine = {
		colors: ['var(--bs-primary)', 'var(--bs-info)'],
		series: [
			{
				name: 'Visitors',
				data: [140, 181, 205, 283, 249, 162, 249, 164, 248, 174, 219, 141]
			},
			{
				name: 'Registrations',
				data: [54, 29, 74, 31, 73, 27, 52, 81, 41, 86, 48, 91]
			}
		],
		chart: {
			height: 350,
			type: 'line',
			fontFamily: 'inherit',
			zoom: {
				enabled: false
			},
			toolbar: {
				show: false
			}
		},
		dataLabels: {
			enabled: false
		},
		stroke: {
			curve: 'stepline',
			width: 3
		},
		grid: {
			strokeDashArray: 4,
			padding: {
				left: 24,
				right: 30,
				bottom: 20
			}
		},
		xaxis: {
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			},
			categories: [
				'Jan',
				'Feb',
				'Mar',
				'Apr',
				'May',
				'Jun',
				'Jul',
				'Aug',
				'Sep',
				'Oct',
				'Nov',
				'Dec'
			]
		},
		yaxis: {
			labels: {
				offsetX: 6
			},
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			}
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: [
				{
					// @ts-ignore
					formatter: function (y) {
						if (typeof y !== 'undefined') {
							return y.toFixed(0) + 'K';
						}
						return y;
					}
				},
				{
					// @ts-ignore
					formatter: function (y) {
						if (typeof y !== 'undefined') {
							return y.toFixed(0) + 'K';
						}
						return y;
					}
				}
			]
		},
		markers: {
			strokeWidth: 5,
			strokeOpacity: 1,
			strokeColors: ['var(--bs-body-bg)', 'var(--bs-body-bg)', 'var(--bs-body-bg)']
		}
	};
	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		// @ts-ignore
		let chart = new ApexCharts(document.querySelector('#chart_line'), optionsLine);
		chart.render();
	});
</script>

<div class="col-12 mb-3 mb-lg-5">
	<div class="card">
		<div class="card-header">
			<h5 class="mb-0">Chart Line</h5>
		</div>
		<!--Chart-->
		<div id="chart_line" />
	</div>
</div>
