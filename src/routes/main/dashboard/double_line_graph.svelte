<script>
	import ApexCharts from 'apexcharts';
	import { onMount } from 'svelte';

	var optionsSalesOverview = {
		colors: ['var(--bs-primary)', 'var(--bs-gray-400)'],
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
				top: 0,
				bottom: 0,
				right: 20
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
				show: true
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
				opacityFrom: 0.05,
				opacityTo: 0,
				stops: [0, 100]
			}
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: {
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
		var chart = new ApexCharts(document.querySelector('#chart_overview'), optionsSalesOverview);
		chart.render();
	});
</script>

<div class="col-xl-9 mb-3 mb-lg-5">
	<div class="card overflow-hidden">
		<div class="card-header d-flex align-items-center">
			<div class="pe-3 flex-grow-1">
				<div class="d-flex align-items-center">
					<h3 class="mb-1">2395</h3>
					<div class="flex-grow-1 ms-3">
						<!--:Badge:-->
						<div class="d-inline-flex align-items-center lh-1 text-success">
							<i class="bi bi-caret-up-fill align-middle text-success" />

							29%
						</div>
					</div>
				</div>
				<p class="mb-0">Sales by Source</p>
			</div>
			<div class="flex-shrink-0">
				<a href="#!" class="btn btn-outline-secondary btn-sm">View Full Report</a>
			</div>
		</div>
		<div class="card-body p-0">
			<div id="chart_overview" />
		</div>
	</div>
</div>
