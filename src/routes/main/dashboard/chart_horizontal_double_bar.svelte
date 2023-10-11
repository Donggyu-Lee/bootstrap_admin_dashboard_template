<script>
	import { onMount } from 'svelte';

	var optionsBar = {
		series: [
			{
				name: 'Revenue',
				data: [23, 27, 18, 21, 19, 25, 23, 27, 18, 21, 19, 23]
			},
			{
				name: 'Expanses',
				data: [-10, -12, -8, -6, -9, -11, -10, -12, -8, -6, -9, -6]
			}
		],
		chart: {
			type: 'bar',
			height: 440,
			stacked: true,
			fontFamily: 'inherit',
			toolbar: {
				show: false
			},
			zoom: {
				enabled: false
			}
		},
		colors: ['var(--bs-primary)', 'var(--bs-warning)'],
		plotOptions: {
			bar: {
				horizontal: true,
				barHeight: '50%',
				borderRadius: [6, 6]
			}
		},
		dataLabels: {
			enabled: false
		},
		stroke: {
			width: 0,
			colors: ['transparent']
		},

		grid: {
			strokeDashArray: 4,
			padding: {
				left: 20,
				right: 30
			},
			xaxis: {
				lines: {
					show: false
				}
			},
			yaxis: {
				lines: {
					show: true
				}
			}
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
			x: {
				// @ts-ignore
				formatter: function (val) {
					return val;
				}
			},
			y: {
				// @ts-ignore
				formatter: function (val) {
					return Math.abs(val) + 'K';
				}
			}
		},
		xaxis: {
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
			],
			labels: {
				// @ts-ignore
				formatter: function (val) {
					return Math.abs(Math.round(val)) + 'K';
				}
			},
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chart_bar'), optionsBar);
		chart.render();
	});
</script>

<div class="col-12 mb-3 mb-lg-5">
	<div class="card">
		<div class="card-header">
			<h5 class="mb-0">Chart Bar</h5>
		</div>
		<!--Chart-->
		<div id="chart_bar" />
	</div>
</div>
