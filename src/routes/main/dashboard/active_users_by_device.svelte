<script>
	import ApexCharts from 'apexcharts';
	import { onMount } from 'svelte';
	import { Tooltip, tooltip } from '@svelte-plugins/tooltips';
	import { browser } from '$app/environment';

	var optionsActiveUsers = {
		series: [
			{
				name: 'Mobile',
				data: [28, 29, 33, 36, 32, 32, 33]
			},
			{
				name: 'Desktop',
				data: [21, 17, 21, 20, 24, 21, 19]
			},
			{
				name: 'Tablet',
				data: [8, 5, 9, 7, 11, 8, 4]
			}
		],
		chart: {
			height: 310,
			type: 'line',
			fontFamily: 'inherit',
			toolbar: {
				show: false
			}
		},
		colors: ['var(--bs-primary)', 'var(--bs-success)', 'var(--bs-danger)'],
		dataLabels: {
			enabled: false
		},
		stroke: {
			width: 3,
			curve: 'smooth'
		},
		grid: {
			strokeDashArray: 4,
			position: 'back',
			padding: {
				right: 30,
				left: 30
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
		markers: {
			strokeWidth: 5,
			strokeOpacity: 1,
			strokeColors: ['var(--bs-body-bg)', 'var(--bs-body-bg)', 'var(--bs-body-bg)']
		},
		xaxis: {
			type: 'category',
			categories: ['Mon', 'Tue', 'Wed', 'Thr', 'Fri', 'Sat', 'Sun'],
			axisTicks: {
				show: true
			},
			axisBorder: {
				show: false
			}
		},
		yaxis: {
			min: 0,
			max: 40,
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			}
		},
		legend: {
			show: false
		},
		tooltip: {
			y: {
				formatter: function (val) {
					return val + 'k <span class="fw-normal text-body-secondary"> Active users</span>';
				}
			}
		}
	};

	onMount(async () => {
		if (browser) {
			var chart = new ApexCharts(document.querySelector('#chart_active_users'), optionsActiveUsers);
			chart.render();
		}
	});
</script>

<div class="col-md-6 mb-3 mb-lg-5">
	<div class="card h-100">
		<div class="card-header">
			<h5 class="mb-0">Active Users by Device</h5>
		</div>
		<div class="row mx-0 text-center">
			<div class="col-12 col-sm border-end-sm border-bottom p-4">
				<p class="mb-1">
					<span class="size-5 bg-primary d-inline-block align-middle me-1 rounded-circle" />
					Mobile
				</p>
				<h5 class="mb-0">10,325</h5>
			</div>
			<div class="col-12 col-sm border-bottom border-end-sm p-4">
				<p class="mb-1">
					<span class="size-5 bg-success d-inline-block align-middle me-1 rounded-circle" />
					Desktop
				</p>
				<h5 class="mb-0">4,235</h5>
			</div>
			<div class="col-12 col-sm p-4 border-bottom">
				<p class="mb-1">
					<span class="size-5 bg-danger d-inline-block align-middle me-1 rounded-circle" />
					Tablet
				</p>
				<h5 class="mb-0">3,575</h5>
			</div>
		</div>
		<div id="chart_active_users" />
	</div>
</div>
