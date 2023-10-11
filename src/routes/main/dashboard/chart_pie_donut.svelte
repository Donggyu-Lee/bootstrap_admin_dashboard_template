<script>
	import { onMount } from 'svelte';
	var optionsPie = {
		colors: ['var(--bs-primary)', 'var(--bs-info)', 'var(--bs-warning)'],
		series: [44, 55, 13],
		chart: {
			type: 'donut',
			fontFamily: 'inherit'
		},
		labels: ['Facebook', 'Twitter', 'Instagram'],
		plotOptions: {
			pie: {
				expandOnClick: false,
				size: 200,
				donut: {
					size: '65%'
				}
			}
		},
		dataLabels: {
			enabled: false,
			dropShadow: {
				enabled: false
			}
		},
		legend: {
			show: false
		},
		tooltip: {
			y: {
				// @ts-ignore
				formatter: function (val) {
					return val + '<span class="fw-normal small">K Followers</span>';
				}
			}
		}
	};

	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		let chart = new ApexCharts(document.querySelector('#chart_pie'), optionsPie);
		chart.render();
	});
</script>

<div class="col-12 col-md-6 mb-3 mb-lg-5">
	<div class="card overflow-hidden">
		<div class="card-header">
			<h5 class="mb-0">Chart Pie Donut</h5>
		</div>
		<div class="row g-0 align-items-center">
			<div class="col">
				<!--::Custom Legends-->
				<div class="card rounded-0 shadow-none border-top-0 border-start-0 border-bottom-0 h-100">
					<!--Custom legend item-->
					<div class="py-4 px-3 border-bottom d-flex align-items-start">
						<span
							class="size-10 flex-shrink-0 mt-1 d-inline-block bg-primary rounded-circle me-2"
						/>
						<div>
							<p class="mb-1 lh-sm text-body-secondary">Facebook</p>
							<h6 class="mb-0">44K Likes</h6>
						</div>
					</div>
					<!--Custom legend item-->
					<div class="py-4 px-3 border-bottom d-flex align-items-start">
						<span class="size-10 flex-shrink-0 mt-1 d-inline-block bg-info rounded-circle me-2" />
						<div>
							<p class="mb-1 lh-sm text-body-secondary">Twitter</p>
							<h6 class="mb-0">55K Followers</h6>
						</div>
					</div>
					<!--Custom legend item-->
					<div class="px-3 py-4 d-flex align-items-start border-bottom border-bottom-md-0">
						<span
							class="size-10 flex-shrink-0 mt-1 d-inline-block bg-warning rounded-circle me-2"
						/>
						<div>
							<p class="mb-1 lh-sm text-body-secondary">Instagram</p>
							<h6 class="mb-0">13K Followers</h6>
						</div>
					</div>
				</div>
				<!--::/End custom legends-->
			</div>
			<div class="col-auto">
				<div
					class="card align-items-center justify-content-center h-100 rounded-0 shadow-none border-0"
				>
					<!--Chart-->
					<div id="chart_pie" />
				</div>
			</div>
		</div>
	</div>
</div>
