<script>
	import { onMount } from 'svelte';

	var options = {
		colors: ['var(--bs-primary)', 'var(--bs-success)'],
		series: [
			{
				name: 'Working Hours',
				data: [48, 36, 29, 39, 54]
			},
			{
				name: 'Tasks Completed',
				data: [214, 198, 121, 111, 139]
			}
		],
		chart: {
			fontFamily: 'inherit',
			height: 350,
			type: 'bar',
			toolbar: {
				show: false
			},
			zoom: {
				enabled: false
			}
		},
		stroke: {
			width: 0,
			dashArray: [4, 0],
			curve: 'smooth'
		},
		markers: {
			strokeWidth: 5,
			strokeOpacity: 1,
			strokeColors: ['var(--bs-body-bg)', 'var(--bs-body-bg)']
		},
		plotOptions: {
			bar: {
				borderRadiusApplication: 'around',
				borderRadiusWhenStacked: 'last',
				columnWidth: '30%',
				distributed: false,
				borderRadius: 11,
				rangeBarOverlap: false,
				rangeBarGroupRows: true
			}
		},
		legend: {
			position: 'top'
		},
		fill: {
			type: 'gradient',
			gradient: {
				shade: 'dark',
				gradientToColors: ['var(--bs-primary)', 'var(--bs-success)'],
				// gradientToColors: [utils.getColor('primary'), utils.getColor('success')],
				shadeIntensity: 0.1,
				type: 'horizontal',
				opacityFrom: 0.95,
				opacityTo: 1,
				stops: [0, 100, 100, 100]
			}
		},
		xaxis: {
			type: 'category',
			categories: ['Mon', 'Tue', 'Wed', 'Thr', 'Fri'],
			tickAmount: 5,

			tooltip: {
				enabled: false
			},
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			},
			labels: {
				offsetX: 0
			}
		},
		yaxis: {
			max: 260,
			min: 0,
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			},
			labels: {
				offsetX: -16
			}
		},
		grid: {
			show: true,
			strokeDashArray: 5,
			padding: {
				left: 0,
				bottom: 0,
				right: 0,
				top: 0
			},
			xaxis: {
				lines: {
					show: false
				}
			},
			yaxis: {
				lines: {
					show: false
				}
			}
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: [
				{
					formatter: function (/** @type {number} */ y) {
						if (typeof y !== 'undefined') {
							return ' : ' + y.toFixed(0) + 'h';
						}
						return y;
					}
				},
				{
					formatter: function (/** @type {number} */ y) {
						if (typeof y !== 'undefined') {
							return ' : ' + y.toFixed(0) + ' Tasks';
						}
						return y;
					}
				}
			]
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chartOverview'), options);
		chart.render();
	});
</script>

<div class="col-md-7 col-lg-8 mb-3 mb-lg-5">
	<div class="card">
		<div class="card-header align-items-center d-flex justify-content-between">
			<h5 class="mb-0">Tasks Overview</h5>
			<nav class="btn-group btn-group-sm nav">
				<a href="#overall" class="btn btn-outline-secondary" data-bs-toggle="tab">Overall</a>
				<a href="#oLastWeek" class="btn btn-outline-secondary active" data-bs-toggle="tab"
					>Last Week</a
				>
			</nav>
		</div>
		<div class="card-body">
			<div class="tab-content">
				<div class="tab-pane fade active show" id="oLastWeek">
					<div id="chartOverview" />
				</div>
				<div class="tab-pane fade" id="overall">
					<div class="d-flex align-items-center justify-content-center">
						<div class="spinner-border" role="status" />
						<span class="ms-3">Loading...</span>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
