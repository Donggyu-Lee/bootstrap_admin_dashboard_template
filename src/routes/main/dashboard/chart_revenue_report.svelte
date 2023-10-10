<script>
	import { onMount } from 'svelte';
	import { Tooltip, tooltip } from '@svelte-plugins/tooltips';
	import { browser } from '$app/environment';

	var optionsRevenue = {
		colors: ['var(--bs-primary)', 'var(--bs-warning)'],
		series: [
			{
				name: 'Revenue',
				data: [147, 190, 230, 198, 274, 190, 366, 277, 173, 209, 164, 190]
			},
			{
				name: 'Expanses',
				data: [-29, -39, -62, -71, -29, -87, -102, -123, -87, -48, -54, -62]
			}
		],
		chart: {
			fontFamily: 'inherit',
			type: 'bar',
			height: 360,
			stacked: true,
			toolbar: {
				show: false
			}
		},
		dataLabels: {
			enabled: false
		},

		plotOptions: {
			bar: {
				columnWidth: '20%',
				startingShapes: 'rounded',
				colors: {
					backgroundBarOpacity: 0
				}
			},
			distributed: true
		},
		grid: {
			strokeDashArray: 6,
			padding: {
				top: 10,
				bottom: 10
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
		tooltip: {
			shared: true,
			intersect: false,
			y: [
				{
					formatter: function (y) {
						if (typeof y !== 'undefined') {
							return ' $' + y.toFixed(0) + 'K';
						}
						return y;
					}
				},
				{
					formatter: function (y) {
						if (typeof y !== 'undefined') {
							return '$' + y.toFixed(0) + 'K';
						}
						return y;
					}
				}
			]
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

			axisTicks: {
				show: true
			},
			axisBorder: {
				show: false
			},
			tooltip: {
				enabled: true
			}
		},
		yaxis: {
			crosshairs: {
				show: false
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		const chart = new ApexCharts(document.querySelector('#chart_revenue_report'), optionsRevenue);
		chart.render();
	});
</script>

<div class="row">
	<div class="col-md-12 col-xl-9 mb-3 mb-lg-5">
		<!--Card-->
		<div class="card overflow-hidden h-100">
			<!--Card header-->
			<div class="d-flex card-header justify-content-between align-items-center">
				<h5 class="mb-0 pe-3">
					Revenue Report
					<i
						class="bi bi-info-circle align-middle ms-2 text-body-secondary fs-6"
						use:tooltip={{
							content: 'Earnings and expanses during the period',
							position: 'bottom',
							autoPosition: true,
							align: 'center',
							animation: 'slide'
						}}
					/>
				</h5>
				<!--Dropdown-->
				<div class="dropdown">
					<a
						href="#"
						data-bs-toggle="dropdown"
						class="btn btn-sm btn-outline-secondary dropdown-toggle"
					>
						2023
					</a>
					<div class="dropdown-menu dropdown-menu-end" style="--bs-dropdown-min-width:7rem">
						<a href="#!" class="active dropdown-item">2023</a>
						<a href="#!" class="dropdown-item">2022</a>
						<a href="#!" class="dropdown-item">2021</a>
						<a href="#!" class="dropdown-item">2020</a>
					</div>
				</div>
			</div>
			<!--Apex chart for Overview-->
			<div class="card-body p-0">
				<!--chart-->
				<div class="w-100">
					<div id="chart_revenue_report" />
				</div>
			</div>
		</div>
	</div>
	<div class="col-xl-3 col-lg-4">
		<!--::begin card-->
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body d-flex align-items-center">
				<!--Card text-->
				<div class="flex-grow-1">
					<div class="h3 mb-2">947</div>
					<span class="text-body-secondary">Products sold</span>
				</div>
				<div class="flex-shrink-0 text-end">
					<div class="small"><span class="text-success">69%</span></div>
					<i class="bi bi-graph-up-arrow text-success fs-4" />
				</div>
			</div>
		</div>
		<!--::/end card-->
		<!--::begin card-->
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body d-flex align-items-center">
				<!--Card text-->
				<div class="flex-grow-1">
					<div class="h3 mb-2">6748</div>
					<span>Unique visitors</span>
				</div>
				<div class="flex-shrink-0 text-end">
					<div class="small"><span class="text-success">124%</span></div>
					<i class="bi bi-graph-up-arrow text-success fs-4" />
				</div>
			</div>
		</div>
		<!--::/end card-->
		<!--::begin card-->
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body d-flex align-items-center">
				<!--Card text-->
				<div class="flex-grow-1">
					<div class="h3 mb-2">5412</div>
					<span>Total Impressions</span>
				</div>
				<div class="flex-shrink-0 text-end">
					<div class="small"><span class="text-danger">9%</span></div>
					<i class="bi bi-graph-down-arrow text-danger fs-4" />
				</div>
			</div>
		</div>
		<!--::/end card-->

		<!--::begin card-->
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body d-flex align-items-center">
				<!--Card text-->
				<div class="flex-grow-1">
					<div class="h3 mb-2">56%</div>
					<span>Conversion rate</span>
				</div>
				<div class="flex-shrink-0 text-end">
					<div class="small"><span class="text-success">35%</span></div>
					<i class="bi bi-graph-up-arrow text-success fs-4" />
				</div>
			</div>
		</div>
		<!--::/end card-->
	</div>
</div>
