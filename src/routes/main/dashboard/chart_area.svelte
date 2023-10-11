<script>
	import { onMount } from 'svelte';

	// @ts-ignore
	var optionsArea = {
		colors: ['var(--bs-primary)', 'var(--bs-warning)'],
		series: [
			{
				name: 'Direct',
				data: [
					144, 155, 187, 156, 261, 247, 163, 144, 155, 257, 156, 261, 224, 163, 144, 155, 257, 156,
					261, 198, 163, 144, 155, 257, 156, 261, 274, 163, 257, 156
				]
			},
			{
				name: 'Ads',
				data: [
					76, 85, 101, 98, 87, 124, 91, 76, 85, 101, 98, 54, 105, 97, 76, 85, 101, 124, 87, 94, 91,
					76, 85, 101, 78, 104, 135, 104, 98, 87
				]
			}
		],

		chart: {
			type: 'area',
			height: 350,
			fontFamily: 'Inherit',
			toolbar: {
				show: false
			}
		},
		dataLabels: {
			enabled: false
		},
		stroke: {
			width: 3,
			curve: 'smooth'
		},
		grid: {
			strokeDashArray: 2,
			padding: {
				left: 16,
				top: 0,
				bottom: 10,
				right: 0
			},
			xaxis: {
				lines: {
					show: true
				}
			},
			yaxis: {
				lines: {
					show: false
				}
			}
		},
		labels: [
			'Jan 1',
			'Jan 2',
			'Jan 3',
			'Jan 4',
			'Jan 5',
			'Jan 6',
			'Jan 7',
			'Jan 8',
			'Jan 9',
			'Jan 10',
			'Jan 11',
			'Jan 12',
			'Jan 13',
			'Jan 14',
			'Jan 15',
			'Jan 16',
			'Jan 17',
			'Jan 18',
			'Jan 19',
			'Jan 20',
			'Jan 21',
			'Jan 22',
			'Jan 23',
			'Jan 24',
			'Jan 25',
			'Jan 26',
			'Jan 27',
			'Jan 28',
			'Jan 29',
			'Jan 30'
		],

		yaxis: {
			labels: {
				show: true,
				offsetX: 6
			}
		},
		xaxis: {
			tickAmount: 6,
			labels: {
				show: true,
				rotate: 0
			},
			tooltip: {
				enabled: false
			},
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			}
		},
		fill: {
			type: 'gradient',
			gradient: {
				shadeIntensity: 1,
				opacityFrom: 0.5,
				opacityTo: 0,
				stops: [0, 100]
			}
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: {
				// @ts-ignore
				formatter: function (val) {
					return val + ' <span class="fw-normal text-body-secondary">Products sold</span>';
				}
			}
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
		let chart = new ApexCharts(document.querySelector('#chart_area'), optionsArea);
		chart.render();
	});
</script>

<div class="col-12 mb-3 mb-lg-5">
	<div class="card">
		<div class="card-header">
			<h5 class="mb-0">Chart Area</h5>
		</div>
		<!--Chart-->
		<div id="chart_area" />
	</div>
</div>
