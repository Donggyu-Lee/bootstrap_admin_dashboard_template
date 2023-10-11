<script>
	import { onMount } from 'svelte';

	// @ts-ignore
	var optionsSparkLineArea = {
		colors: ['var(--bs-border-color)'],
		series: [
			{
				name: 'Sales',
				data: [44, 32, 37, 42, 28, 39, 35]
			}
		],
		chart: {
			fontFamily: 'inherit',
			type: 'area',
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
			width: 0,
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
		fill: {
			type: 'solid',
			gradient: {}
		},
		tooltip: {
			shared: true,
			intersect: false,
			y: {
				// @ts-ignore
				formatter: function (val) {
					return val + 'K <span class="fw-normal text-body-secondary"> Sales</span>';
				}
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		// @ts-ignore
		let chart = new ApexCharts(
			document.querySelector('#chart_sparkline_area'),
			optionsSparkLineArea
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
				class="size-50 me-3 flex-shrink-0 bg-primary-subtle d-flex align-items-center justify-content-center rounded-pill text-primary"
			>
				<i class="bi bi-cart4 fs-3" />
			</div>
			<div class="flex-grow-1">
				<h3 class="mb-1">147.3K</h3>
				<p class="mb-0">Sales</p>
			</div>
		</div>
		<div class="rounded-bottom overflow-hidden">
			<!--chart-->
			<div id="chart_sparkline_area" class="rounded-bottom" />
		</div>
	</div>
	<!--/::end card-->
</div>
