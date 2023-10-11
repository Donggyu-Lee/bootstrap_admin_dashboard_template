<script>
	import { onMount } from 'svelte';

	var optionsSparkLineBar = {
		colors: ['var(--bs-success)'],
		series: [
			{
				name: 'Conversion',
				data: [54, 62, 68, 63, 59, 32, 24]
			}
		],
		chart: {
			fontFamily: 'inherit',
			type: 'bar',
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
		plotOptions: {
			bar: {
				columnWidth: '40%',
				borderRadius: 4
			}
		},
		dataLabels: {
			enabled: false
		},
		stroke: {
			width: 0,
			color: 'transparent'
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
				// @ts-ignore
				formatter: function (val) {
					return val + '%';
				}
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chart_sparkline_bar'), optionsSparkLineBar);
		chart.render();
	});
</script>

<div class="col-md-4 mb-3 mb-lg-5">
	<!--/::begin card-->
	<div class="card">
		<div class="card-body p-4 pb-3 d-flex align-items-center justify-content-between">
			<!--Icon-->
			<div
				class="size-50 me-3 flex-shrink-0 bg-success-subtle text-success d-flex align-items-center justify-content-center rounded-pill"
			>
				<i class="bi bi-cart4 fs-3" />
			</div>
			<div class="flex-grow-1">
				<h3 class="mb-1">56%</h3>
				<p class="mb-0">Conversion rate</p>
			</div>
		</div>
		<div class="rounded-bottom">
			<!--chart-->
			<div id="chart_sparkline_bar" class="rounded-bottom" />
		</div>
	</div>
	<!--/::end card-->
</div>
