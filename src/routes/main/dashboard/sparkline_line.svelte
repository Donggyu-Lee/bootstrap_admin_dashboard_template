<script>
	import { onMount } from 'svelte';

	var optionsSparkLineLine = {
		colors: ['var(--bs-warning)'],
		series: [
			{
				name: 'Earnings',
				data: [23, 21, 24, 25, 22, 16, 12]
			}
		],
		chart: {
			fontFamily: 'inherit',
			type: 'line',
			height: 120,
			zoom: {
				enabled: false
			},
			toolbar: {
				show: false
			},
			sparkline: {
				enabled: true
			}
		},
		dataLabels: {
			enabled: false
		},
		stroke: {
			width: 2,
			curve: 'smooth'
		},
		markers: {
			strokeWidth: 5,
			strokeOpacity: 1,
			strokeColors: ['var(--bs-body-bg)']
		},
		labels: ['Mon', 'Tue', 'Wed', 'Thr', 'Fri', 'Sat', 'Sun'],
		xaxis: {
			type: 'category'
		},
		yaxis: {
			opposite: true
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: {
				formatter: function (/** @type {string} */ val) {
					return '$' + val + 'K <span class="fw-normal text-body-secondary"> Thousands</span>';
				}
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(
			document.querySelector('#chart_sparkline_line'),
			optionsSparkLineLine
		);
		chart.render();
	});
</script>

<div class="col-md-4 mb-3 mb-lg-5">
	<!--/::begin card-->
	<div class="card">
		<div class="card-body p-4 pb-3 d-flex align-items-center justify-content-between">
			<!--Icon-->
			<div
				class="size-50 me-3 flex-shrink-0 bg-warning-subtle text-warning d-flex align-items-center justify-content-center rounded-pill"
			>
				<i class="bi bi-cart4 fs-3" />
			</div>
			<div class="flex-grow-1">
				<h3 class="mb-1">$421.7K</h3>
				<p class="mb-0">Earnings</p>
			</div>
		</div>
		<div class="rounded-bottom">
			<!--chart-->
			<div id="chart_sparkline_line" class="rounded-bottom" />
		</div>
	</div>
	<!--/::end card-->
</div>
