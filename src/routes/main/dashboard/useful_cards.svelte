<script>
	// @ts-ignore
	import { Tooltip, tooltip } from '@svelte-plugins/tooltips';

	import sample_image_1 from '$lib/images/AttnKare_logo.webp';
	import sample_image_2 from '$lib/images/BlueKare_logo.webp';
	import sample_image_3 from '$lib/images/profile_photo.jpeg';
	import sample_image_4 from '$lib/images/hippo_logo_icon_only.png';

	import flag_us from '$lib/images/flags/united-states.svg';
	import flag_uk from '$lib/images/flags/united-kingdom.svg';
	import flag_poland from '$lib/images/flags/poland.svg';
	import flag_korea from '$lib/images/flags/south-korea.svg';
	import flag_spain from '$lib/images/flags/spain.svg';
	import flag_kenya from '$lib/images/flags/kenya.svg';
	import flag_france from '$lib/images/flags/france.svg';
	import flag_china from '$lib/images/flags/china.svg';
	import flag_vietnam from '$lib/images/flags/vietnam.svg';
</script>

<div class="row mb-5">
	<!-- 숫자 카드 -->
	<div class="col-sm-6 col-xl-3">
		<div class="card card-body mb-3 mb-lg-5">
			<div class="d-flex justify-content-between align-items-center">
				<div class="me-3">
					<h5 class="fs-4">847059</h5>
					<span class="text-body-secondary">Sales earnings</span>
				</div>
				<div
					class="text-white bg-primary flex-shrink-0 size-50 rounded-2 d-flex align-items-center justify-content-center"
				>
					<i class="bi bi-currency-dollar fs-3" />
				</div>
			</div>
		</div>
	</div>

	<!-- 프로그레스 바 카드 -->
	<div class="col-sm-6 col-xl-3">
		<div class="card card-body mb-3 mb-lg-5">
			<div class="row align-items-center">
				<div class="col">
					<p class="text-body-secondary d-block mb-2">Project Progress</p>
					<div class="progress bg-primary-subtle mb-1" style="height: 4px;">
						<div class="progress-bar bg-primary" style="width: 30%;" role="progressbar" />
					</div>
					<h4 class="mb-0">30%</h4>
				</div>
				<div class="col-auto text-primary">
					<div
						class="text-success bg-success-subtle flex-shrink-0 size-50 rounded-2 d-flex align-items-center justify-content-center"
					>
						<i class="bi bi-clipboard-check fs-3" />
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- 숫자+% 카드  -->
	<div class="col-sm-6 col-xl-3">
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body d-flex align-items-center">
				<div class="flex-grow-1">
					<h5 class="fs-4 mb-1">847059</h5>
					<span class="text-body-secondary">Sales earnings</span>
				</div>
				<div class="flex-shrink-0 text-end align-items-center justify-content-center">
					<div class="small"><span class="text-success">+35%</span></div>
					<i class="bi bi-graph-up-arrow text-success fs-3" />
				</div>
			</div>
		</div>
	</div>

	<!-- 숫자 카드 -->
	<div class="col-sm-6 col-xl-3">
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body d-flex align-items-center">
				<div class="flex-grow-1">
					<h5 class="fs-4 mb-1">1425</h5>
					<span class="text-body-secondary">Total Sales</span>
				</div>
				<div class="flex-shrink-0 ps-4 border-start">
					<i class="bi bi-tag fs-3 text-primary" />
				</div>
			</div>
		</div>
	</div>

	<!-- 프로그레스바(red) 카드 -->
	<div class="col-xl-4 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body">
				<h5 class="mb-2">Company finance</h5>
				<div class="progress bg-danger-subtle mb-1" style="height: 4px;">
					<div class="progress-bar bg-danger" style="width: 68%;" role="progressbar" />
				</div>
				<div class="flex-grow-1 d-flex align-items-center">
					<h5 class="fs-4 mb-0">64</h5>
					<span class="text-body-secondary small ms-auto">Used</span>
				</div>
			</div>
		</div>
	</div>

	<!-- 프로그레스바(green) 카드 -->
	<div class="col-xl-4 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body">
				<h5 class="mb-2">Storage</h5>
				<div class="progress bg-success-subtle mb-1" style="height: 4px;">
					<div class="progress-bar bg-success" style="width: 37%;" role="progressbar" />
				</div>
				<div class="flex-grow-1 d-flex align-items-center">
					<h5 class="fs-4 mb-0">37</h5>
					<span class="text-body-secondary small ms-auto">Used of 100GB</span>
				</div>
			</div>
		</div>
	</div>

	<!-- 프로그레스바(two color) 카드 -->
	<div class="col-xl-4 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body">
				<h5 class="mb-2">Task Overview</h5>
				<div class="progress mb-3" style="height: 4px;">
					<div class="progress-bar bg-primary" style="width: 63%;" role="progressbar" />
					<div class="progress-bar bg-warning" style="width: 37%;" role="progressbar" />
				</div>
				<ul class="list-unstyled d-flex mb-0">
					<li class="d-flex align-items-center me-4">
						<span class="bg-primary size-5 rounded-circle me-2" />
						<span class="text-body-secondary small">Finished</span>
					</li>
					<li class="d-flex align-items-center me-4">
						<span class="bg-warning size-5 rounded-circle me-2" />
						<span class="text-body-secondary small">Due</span>
					</li>
				</ul>
			</div>
		</div>
	</div>

	<!-- 넓은 숫자 카드(파란배경) -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card bg-primary border-primary text-white overflow-hidden">
			<div class="card-body">
				<i class="bi bi-people align-middle fs-1 mb-2" />
				<h5 class="fs-4 mb-1">8475</h5>
				<h6 class="mb-0 text-reset fw-normal">New customers</h6>
			</div>
		</div>
	</div>

	<!-- 넓은 숫자 카드 (분홍 배경) -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card bg-danger-subtle text-body border-0 overflow-hidden">
			<div class="card-body">
				<i class="bi bi-people align-middle fs-1 mb-2" />
				<h5 class="fs-4 mb-1">647</h5>
				<h6 class="mb-0 fw-normal">New customers</h6>
			</div>
		</div>
	</div>

	<!-- 넓은 숫자 카드 (흰 배경) -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body">
				<i class="bi bi-people align-middle fs-1 mb-2" />
				<h5 class="fs-4 mb-1">9478</h5>
				<h6 class="mb-0 text-body-secondary fw-normal">New customers</h6>
			</div>
		</div>
	</div>

	<!-- 넓은 숫자 카드 (흰 배경+테두리) -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card border-primary-subtle text-body overflow-hidden">
			<div class="card-body">
				<i class="bi bi-people align-middle fs-1 mb-2" />
				<h5 class="fs-4 mb-1">678</h5>
				<h6 class="mb-0 text-body-secondary fw-normal">New customers</h6>
			</div>
		</div>
	</div>

	<!-- 숫자 카드(왼쪽 아이콘) -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body d-flex align-items-center justify-content-between">
				<div
					class="flex-shrink-0 size-60 bg-primary-subtle text-primary rounded-pill me-3 d-flex align-items-center justify-content-center"
				>
					<i class="bi bi-people align-middle fs-2" />
				</div>
				<div class="flex-grow-1 text-start">
					<h5 class="fs-4 mb-1">254</h5>
					<h6 class="mb-0 fw-normal">New customers</h6>
				</div>
			</div>
		</div>
	</div>

	<!-- 숫자 카드 -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body d-flex align-items-center justify-content-between">
				<div
					class="flex-shrink-0 size-60 bg-success-subtle text-success rounded-pill me-3 d-flex align-items-center justify-content-center"
				>
					<i class="bi bi-currency-dollar fs-2" />
				</div>
				<div class="flex-grow-1 text-start">
					<h5 class="fs-4 d-block mb-1">$38382</h5>
					<h6 class="mb-0 fw-normal">Revenue</h6>
				</div>
			</div>
		</div>
	</div>

	<!-- 숫자 카드(상단 컬러) -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div
				class="card-body border-top border-4 border-primary d-flex align-items-center justify-content-between"
			>
				<div
					class="flex-shrink-0 size-60 bg-primary text-white rounded-pill me-3 d-flex align-items-center justify-content-center"
				>
					<!-- <i class="bi bi-chevron-down fs-2" /> -->
					<i class="bi bi-chevron-up fs-2" />
				</div>
				<div class="flex-grow-1 text-start">
					<h5 class="fs-4 d-block mb-1">38%</h5>
					<h6 class="mb-0 fw-normal">Bounce Rate</h6>
				</div>
			</div>
		</div>
	</div>

	<!-- 숫자카드 -->
	<div class="col-xl-3 col-md-6 mb-3 mb-lg-5">
		<div class="card overflow-hidden">
			<div class="card-body d-flex align-items-center justify-content-between">
				<div
					class="flex-shrink-0 size-60 bg-success text-white rounded-pill me-3 d-flex align-items-center justify-content-center"
				>
					<!-- <i class="bi bi-chevron-down fs-2" /> -->
					<i class="bi bi-chevron-up fs-2" />
				</div>
				<div class="flex-grow-1 text-start">
					<h5 class="fs-4 d-block mb-1">65%</h5>
					<h6 class="mb-0 fw-normal">Bounce Rate</h6>
				</div>
			</div>
		</div>
	</div>
</div>

<div class="row">
	<div class="col-sm-6 col-xl-3 mb-3 mb-lg-5">
		<!--::begin card-->
		<div class="card card-body">
			<!--Title-->
			<h6 class="mb-3">
				New Orders
				<i
					class="bi bi-info-circle ms-2 fs-6 align-middle opacity-75"
					use:tooltip={{
						content: 'New orders received in last month',
						position: 'top',
						autoPosition: true,
						align: 'center',
						animation: 'slide',
						theme: 'tippy-box'
					}}
				/>
			</h6>
			<div class="d-flex lh-1 align-items-center">
				<h4 class="mb-0">245</h4>

				<!--vertical line-->
				<div
					class="vr lh-1 align-self-center opacity-25 mx-3 height-10"
					style="min-height: auto;"
				/>
				<!--::/vertical line-->

				<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-success" />
				<small>11%</small>
			</div>
		</div>
		<!--::/end card-->
	</div>
	<div class="col-sm-6 col-xl-3 mb-3 mb-lg-5">
		<!--::begin card-->
		<div class="card card-body">
			<!--Title-->
			<h6 class="mb-3">
				Earnings
				<i
					class="bi bi-info-circle ms-2 fs-6 align-middle opacity-75"
					use:tooltip={{
						content: 'New orders received',
						position: 'top',
						autoPosition: true,
						align: 'center',
						animation: 'slide',
						theme: 'tippy-box'
					}}
				/>
			</h6>
			<div class="d-flex lh-1 align-items-center">
				<h4 class="mb-0">$756,689</h4>
				<div
					class="vr lh-1 align-self-center opacity-25 mx-3 height-10"
					style="min-height: auto;"
				/>
				<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-success" />
				<small>36%</small>
			</div>
		</div>
	</div>
	<div class="col-sm-6 col-xl-3 mb-3 mb-lg-5">
		<div class="card card-body">
			<h6 class="mb-3">
				Return
				<i
					class="bi bi-info-circle ms-2 fs-6 align-middle opacity-75"
					use:tooltip={{
						content: 'Products returns',
						position: 'top',
						autoPosition: true,
						align: 'center',
						animation: 'slide',
						theme: 'tippy-box'
					}}
				/>
			</h6>
			<div class="d-flex lh-1 align-items-center">
				<h4 class="mb-0">87</h4>
				<div
					class="vr lh-1 align-self-center opacity-25 mx-3 height-10"
					style="min-height: auto;"
				/>
				<i class="bi bi-caret-down-fill align-middle fs-5 me-1 text-danger" />
				<small>47%</small>
			</div>
		</div>
	</div>
	<div class="col-sm-6 col-xl-3 mb-3 mb-lg-5">
		<div class="card card-body">
			<h6 class="mb-3">
				Conversion Rate
				<i
					class="bi bi-info-circle ms-2 fs-6 align-middle opacity-75"
					use:tooltip={{
						content: 'Visitors who purchased at least 1 product',
						position: 'top',
						autoPosition: true,
						align: 'center',
						animation: 'slide',
						theme: 'tippy-box'
					}}
				/>
			</h6>
			<div class="d-flex lh-1 align-items-center">
				<h4 class="mb-0">67%</h4>
				<div
					class="vr lh-1 align-self-center opacity-25 mx-3 height-10"
					style="min-height: auto;"
				/>
				<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-success" />
				<small>24%</small>
			</div>
		</div>
	</div>

	<div class="col-xl-6 mb-3 mb-lg-5">
		<div class="card overflow-hidden mb-3 mb-lg-5">
			<div class="card-body">
				<div class="mb-3 d-flex align-items-center overflow-hidden">
					<div>
						<p class="mb-0 text-truncate">Customers Rate</p>
					</div>
					<div class="ps-3 ms-auto">
						<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-success" /> 18%
					</div>
				</div>
				<div class="flex-shrink-0 ms-auto">
					<div class="progress height-10 mb-3">
						<div
							class="progress-bar"
							role="progressbar"
							aria-label="Segment one"
							style="width: 57%"
						/>
						<div
							class="progress-bar bg-success"
							role="progressbar"
							aria-label="Segment two"
							style="width: 43%"
						/>
					</div>
					<div class="d-flex align-items-center">
						<div class="flex-grow-1">
							<h5 class="mb-0">57%</h5>
							<span class="small text-body-secondary"> First time buyers </span>
						</div>
						<div class="text-end">
							<h5 class="mb-0">43%</h5>
							<span class="small text-body-secondary"> Returning </span>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="card card-body">
			<div class="mb-auto">
				<div class="d-flex align-items-staretch">
					<div class="flex-grow-1">
						<h3>39</h3>
						<p class="mb-4">Active Projects</p>
					</div>
					<div class="flex-shrink-0">
						<a href="#!" class="btn btn-primary btn-sm">Manage</a>
					</div>
				</div>
			</div>
			<div class="mt-auto">
				<div class="d-flex align-items-center justify-content-between">
					<p class="mb-0 fw-semibold">Pending</p>
					<p class="mb-0 fw-semibold">17%</p>
				</div>
				<div class="progress mt-2 height-5">
					<div
						class="progress-bar bg-primary rounded-pill progress-bar-striped progress-bar-animated"
						role="progressbar"
						aria-label="Animated striped example"
						style="width: 17%"
					/>
				</div>
			</div>
		</div>
	</div>
</div>
