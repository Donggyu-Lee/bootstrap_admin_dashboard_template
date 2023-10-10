<script>
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

	import ChartRevenueReport from './chart_revenue_report.svelte';
	import ProjectStats from './project_stats.svelte';
	import UsefulCards from './useful_cards.svelte';
	import ActiveUsersByDevice from './active_users_by_device.svelte';
	import DoubleLineGraph from './double_line_graph.svelte';
	import DoubleBarGraph from './double_bar_graph.svelte';
	import { onMount } from 'svelte';
</script>

<div class="container-fluid pb-0 pt-3 px-3 px-lg-6 d-flex flex-column-fluid">
	<div class=" px-0">
		<div class=" px-0">
			<div class="d-flex mb-7 align-items-center">
				<div class="flex-grow-1 border-top border-gray" />
				<h5 class="flex-shrink-0 mb-0 px-3">Project Widgets</h5>
				<div class="flex-grow-1 border-top border-gray" />
			</div>
			<div class="row mb-5">
				<!-- 프로젝트 위젯 카드 -->
				<div class="col-xl-4 mb-3 mb-lg-5">
					<div class="card">
						<div class="d-flex card-header justify-content-between align-items-center">
							<h5 class="pe-3 mb-0">Projects</h5>
							<span>
								<a href="#!.html">View All</a>
							</span>
						</div>
						<div class="card-body p-0">
							<ul class="list-group list-group-flush mb-0">
								<!--List group-item begin-->
								<li class="list-group-item bg-transparent px-3">
									<div class="d-flex align-items-center">
										<div class="flex-shrink-0 me-3">
											<a href="#!.html">
												<img
													src={sample_image_1}
													class="img-fluid rounded-2 width-80 h-auto"
													alt=""
												/>
											</a>
										</div>
										<div class="overflow-hidden flex-grow-1">
											<h6 class="mb-0 text-truncate">
												<a href="#!.html" class="text-reset">Podcaster music site</a>
											</h6>
											<span class="text-body-secondary text-truncate d-block"
												>Lorem ipsum dolor sit amet uses for print</span
											>
										</div>
										<div class="">
											<!--Dropdown-->
											<div class="dropdown d-block">
												<a
													href="#"
													data-bs-toggle="dropdown"
													class="text-body-secondary d-block lh-1"
												>
													<i class="bi bi-three-dots-vertical" />
												</a>
												<div class="dropdown-menu dropdown-menu-end mt-1">
													<a href="#!.html" class="dropdown-item">Action</a>
													<a href="#!.html" class="dropdown-item">Another action</a>
													<a href="#!.html" class="dropdown-item">Something else</a>
												</div>
											</div>
										</div>
									</div>
								</li>

								<!--List group-item begin-->
								<li class="list-group-item bg-transparent px-3">
									<div class="d-flex align-items-center">
										<div class="flex-shrink-0 me-3">
											<a href="#!.html">
												<img
													src={sample_image_2}
													class="img-fluid rounded-2 width-80 h-auto"
													alt=""
												/>
											</a>
										</div>
										<div class="overflow-hidden flex-grow-1">
											<h6 class="mb-0 text-truncate">
												<a href="#!.html" class="text-reset">Plainting online store</a>
											</h6>
											<span class="text-body-secondary text-truncate d-block"
												>Lorem ipsum dolor sit amet uses for print</span
											>
										</div>
										<div class="">
											<!--Dropdown-->
											<div class="dropdown d-block">
												<a
													href="#"
													data-bs-toggle="dropdown"
													class="text-body-secondary d-block lh-1"
												>
													<i class="bi bi-three-dots-vertical" />
												</a>
												<div class="dropdown-menu dropdown-menu-end mt-1">
													<a href="#!.html" class="dropdown-item">Action</a>
													<a href="#!.html" class="dropdown-item">Another action</a>
													<a href="#!.html" class="dropdown-item">Something else</a>
												</div>
											</div>
										</div>
									</div>
								</li>

								<!--List group-item begin-->
								<li class="list-group-item bg-transparent px-3">
									<div class="d-flex align-items-center">
										<div class="flex-shrink-0 me-3">
											<a href="#!.html">
												<img
													src={sample_image_1}
													class="img-fluid rounded-2 width-80 h-auto"
													alt=""
												/>
											</a>
										</div>
										<div class="overflow-hidden flex-grow-1">
											<h6 class="mb-0 text-truncate">
												<a href="#!.html" class="text-reset">Has branding</a>
											</h6>
											<span class="text-body-secondary text-truncate d-block"
												>Lorem ipsum dolor sit amet uses for print</span
											>
										</div>
										<div class="">
											<!--Dropdown-->
											<div class="dropdown d-block">
												<a
													href="#"
													data-bs-toggle="dropdown"
													class="text-body-secondary d-block lh-1"
												>
													<i class="bi bi-three-dots-vertical" />
												</a>
												<div class="dropdown-menu dropdown-menu-end mt-1">
													<a href="#!.html" class="dropdown-item">Action</a>
													<a href="#!.html" class="dropdown-item">Another action</a>
													<a href="#!.html" class="dropdown-item">Something else</a>
												</div>
											</div>
										</div>
									</div>
								</li>

								<!--List group-item begin-->
								<li class="list-group-item bg-transparent px-3">
									<div class="d-flex align-items-center">
										<div class="flex-shrink-0 me-3">
											<a href="#!.html">
												<img
													src={sample_image_1}
													class="img-fluid rounded-2 width-80 h-auto"
													alt=""
												/>
											</a>
										</div>
										<div class="overflow-hidden flex-grow-1">
											<h6 class="mb-0 text-truncate">
												<a href="#!.html" class="text-reset">Project title</a>
											</h6>
											<span class="text-body-secondary text-truncate d-block"
												>Lorem ipsum dolor sit amet uses for print</span
											>
										</div>
										<div class="">
											<!--Dropdown-->
											<div class="dropdown d-block">
												<a
													href="#"
													data-bs-toggle="dropdown"
													class="text-body-secondary d-block lh-1"
												>
													<i class="bi bi-three-dots-vertical" />
												</a>
												<div class="dropdown-menu dropdown-menu-end mt-1">
													<a href="#!.html" class="dropdown-item">Action</a>
													<a href="#!.html" class="dropdown-item">Another action</a>
													<a href="#!.html" class="dropdown-item">Something else</a>
												</div>
											</div>
										</div>
									</div>
								</li>
							</ul>
						</div>
					</div>
				</div>

				<!-- 이미지 + 프로그레스 + 프로필 카드 -->
				<div class="col-xl-4 mb-3 mb-lg-5">
					<div class="card">
						<!-- Card Image -->
						<a href="#!.html">
							<img src={sample_image_1} alt="..." class="card-img-top" />
						</a>

						<!-- Card - Body -->
						<div class="card-body mt-0">
							<div class="row align-items-center">
								<div class="col">
									<h6 class="mb-1">
										<a href="#!.html" class="text-reset">CRM dashboard</a>
									</h6>
									<small class="text-body-secondary"> Updated yestarday </small>
								</div>
								<div class="col-auto">
									<!-- Dropdown -->
									<div class="dropdown">
										<a
											href="#"
											class="text-body-secondary d-block lh-1"
											role="button"
											data-bs-toggle="dropdown"
											aria-haspopup="true"
											aria-expanded="false"
										>
											<i class="bi bi-three-dots-vertical" />
										</a>
										<div class="dropdown-menu mt-1 dropdown-menu-end">
											<a href="#!" class="dropdown-item"> Action </a>
											<a href="#!" class="dropdown-item"> Another action </a>
											<a href="#!" class="dropdown-item"> Something else </a>
										</div>
									</div>
								</div>
							</div>
						</div>

						<!--card Footer -->
						<div class="card-footer">
							<div class="row align-items-center">
								<div class="col">
									<div class="row align-items-center g-0">
										<div class="col-auto">
											<small class="me-2">65%</small>
										</div>
										<div class="col">
											<!-- Progress bar -->
											<div class="progress bg-success-subtle" style="height: 4px;">
												<div
													class="progress-bar bg-success"
													role="progressbar"
													style="width: 65%;"
												/>
											</div>
										</div>
									</div>
								</div>

								<div class="col-auto">
									<!-- Avatars group -->
									<div class="avatar-group justify-content-end">
										<a
											href="#!.html"
											class="avatar-group-item avatar sm rounded-circle"
											use:tooltip={{
												content: '홍길동',
												position: 'top',
												autoPosition: true,
												align: 'center',
												animation: 'slide',
												theme: 'tippy-box'
											}}
										>
											<img src={sample_image_3} alt="..." class="avatar-group-img rounded-circle" />
										</a>
										<a
											href="#!.html"
											class="avatar-group-item avatar sm rounded-circle"
											use:tooltip={{
												content: '홍길동',
												position: 'top',
												autoPosition: true,
												align: 'center',
												animation: 'slide',
												theme: 'tippy-box'
											}}
										>
											<img src={sample_image_3} alt="..." class="avatar-group-img rounded-circle" />
										</a>
										<a
											href="#!.html"
											class="avatar-group-item avatar sm rounded-circle"
											use:tooltip={{
												content: '홍길동',
												position: 'top',
												autoPosition: true,
												align: 'center',
												animation: 'slide',
												theme: 'tippy-box'
											}}
										>
											<img src={sample_image_3} alt="..." class="avatar-group-img rounded-circle" />
										</a>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>

				<!-- -->

				<!-- -->
				<!-- -->
				<!-- -->
				<!-- -->
				<!-- -->
				<!-- -->
				<!-- -->
				<!-- -->
			</div>

			<div class=" px-0">
				<div class="d-flex mb-7 align-items-center">
					<div class="flex-grow-1 border-top border-gray" />
					<h5 class="flex-shrink-0 mb-0 px-3">User Widgets</h5>
					<div class="flex-grow-1 border-top border-gray" />
				</div>
				<div class="row mb-5">
					<div class="col-md-6 mb-3 mb-lg-5">
						<div class="card">
							<!--Card title-->
							<div class="d-flex card-header justify-content-between align-items-center">
								<h5 class="mb-0 me-3">Users</h5>
								<a href="#!.html">View All</a>
							</div>

							<div class="card-body py-0">
								<!--List-->
								<ul class="list-group list-group-flush">
									<!--List group item-->
									<li class="list-group-item">
										<div class="row align-items-center">
											<div class="col-auto">
												<a href="#!" class="">
													<div class="avatar avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</div>
												</a>
											</div>
											<div class="col">
												<h6 class="mb-0"><a href="#!.html">Jason Momoa</a></h6>
												<small class="text-body-secondary">Front end developer</small>
											</div>
											<div class="col-auto">
												<a href="#!.html" class="btn btn-sm btn-outline-primary">Add</a>
											</div>
										</div>
									</li>
									<!--List group item-->
									<li class="list-group-item">
										<div class="row align-items-center">
											<div class="col-auto">
												<a href="#!" class="">
													<div class="avatar avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</div>
												</a>
											</div>
											<div class="col">
												<h6 class="mb-0"><a href="#!.html">Emily Doe</a></h6>
												<small class="text-body-secondary">Front end developer</small>
											</div>
											<div class="col-auto">
												<a href="#!.html" class="btn btn-sm btn-outline-primary">Add</a>
											</div>
										</div>
									</li>
									<!--List group item-->
									<li class="list-group-item">
										<div class="row align-items-center">
											<div class="col-auto">
												<a href="#!" class="">
													<div class="avatar avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</div>
												</a>
											</div>
											<div class="col">
												<h6 class="mb-0"><a href="#!.html">Danzel Walsh</a></h6>
												<small class="text-body-secondary">Python developer</small>
											</div>
											<div class="col-auto">
												<a href="#!.html" class="btn btn-sm btn-outline-primary">Add</a>
											</div>
										</div>
									</li>
								</ul>
							</div>
						</div>
					</div>

					<!-- -->
					<div class="col-md-6 mb-3 mb-lg-5">
						<div class="card card-body">
							<!--List-->
							<ul class="list-group list-group-flush">
								<!--List group item-->
								<li class="list-group-item">
									<div class="row align-items-center">
										<div class="col-auto">
											<a href="#!" class="">
												<div class="avatar">
													<img
														src={sample_image_3}
														class="img-fluid rounded-circle w-auto"
														alt=""
													/>
												</div>
											</a>
										</div>
										<div class="col">
											<h6 class="mb-0"><a href="#!.html" class="text-reset">Nikita Miller</a></h6>
											<span class="text-body-secondary small d-flex align-items-center"
												><span
													class="align-middle me-1 size-5 border border-4 border-warning rounded-circle d-inline-block"
												/>
												Away</span
											>
										</div>
										<div class="col-auto">
											<a href="#!.html" class="btn btn-sm btn-outline-primary">Follow</a>
										</div>
									</div>
								</li>
								<!--List group item-->
								<li class="list-group-item">
									<div class="row align-items-center">
										<div class="col-auto">
											<a href="#!" class="">
												<div class="avatar">
													<img
														src={sample_image_3}
														class="img-fluid rounded-circle w-auto"
														alt=""
													/>
												</div>
											</a>
										</div>
										<div class="col">
											<h6 class="mb-0"><a href="#!.html" class="text-reset">Josefh Ansari</a></h6>
											<span class="text-body-secondary small d-flex align-items-center"
												><span
													class="align-middle me-1 size-5 border border-4 border-success rounded-circle d-inline-block"
												/>
												Online</span
											>
										</div>
										<div class="col-auto">
											<a href="#!.html" class="btn btn-sm btn-outline-primary">Follow</a>
										</div>
									</div>
								</li>
								<!--List group item-->
								<li class="list-group-item">
									<div class="row align-items-center">
										<div class="col-auto">
											<a href="#!" class="">
												<div class="avatar">
													<img
														src={sample_image_3}
														class="img-fluid rounded-circle w-auto"
														alt=""
													/>
												</div>
											</a>
										</div>
										<div class="col">
											<h6 class="mb-0"><a href="#!.html" class="text-reset">Jason Momoa</a></h6>
											<span class="text-body-secondary small d-flex align-items-center"
												><span
													class="align-middle me-1 size-5 border border-4 border-success rounded-circle d-inline-block"
												/>
												Online</span
											>
										</div>
										<div class="col-auto">
											<a href="#!.html" class="btn btn-sm btn-outline-primary">Follow</a>
										</div>
									</div>
								</li>
							</ul>
						</div>
					</div>

					<!-- -->

					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
				</div>
				<div class=" px-0">
					<div class="d-flex mb-7 align-items-center">
						<div class="flex-grow-1 border-top border-gray" />
						<h5 class="flex-shrink-0 mb-0 px-3">Activity Widgets</h5>
						<div class="flex-grow-1 border-top border-gray" />
					</div>
					<div class="row mb-5">
						<!-- -->
						<div class="col-12 col-lg-6 mb-3 mb-lg-5">
							<div class="card overflow-hidden">
								<div class="card-header">
									<h5 class="card-title mb-0">Notifications</h5>
								</div>
								<div class="card-body p-0">
									<ul class="list-group list-group-flush mb-0">
										<li
											class="px-3 pt-3 pb-0 list-group-item h6 text-body-tertiary border-bottom-0"
										>
											New
										</li>
										<!--//Notification item start//-->
										<li class="list-group-item">
											<a
												href="#"
												class="list-group-item-action px-3 py-2 text-reset d-flex align-items-center"
											>
												<div class="d-block me-3">
													<div class="avatar avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</div>
												</div>

												<div class="flex-grow-1 flex-wrap pe-3">
													<span class="mb-0 d-block"
														><strong>Adam Danely</strong> assigned a task to you
														<strong>#PI-392</strong></span
													>
													<small class="text-body-secondary">Just now</small>
												</div>
											</a>
										</li>
										<!--//Notification item start//-->
										<li class="list-group-item">
											<a
												href="#"
												class="list-group-item-action px-3 py-2 text-reset d-flex align-items-center"
											>
												<div class="d-block me-3">
													<div class="avatar avatar-status status-offline">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</div>
												</div>

												<div class="flex-grow-1 flex-wrap pe-3">
													<span class="mb-0 d-block"
														><strong>Vivianna Kiser </strong> just posted
														<span
															>"Lorem ipsum is placeholder text used in the graphic, print, and
															industries. "</span
														></span
													>
													<small class="text-body-secondary">2h Ago</small>
												</div>
											</a>
										</li>

										<li
											class="px-3 pt-3 pb-0 h6 list-group-item text-body-tertiary border-bottom-0"
										>
											Earlier
										</li>
										<!--//Notification item start//-->
										<li class="list-group-item">
											<a
												href="#"
												class="list-group-item-action px-3 py-2 text-reset d-flex align-items-center"
											>
												<span class="d-block me-3">
													<span
														class="d-flex align-items-center justify-content-center lh-1 size-50 bg-success-subtle text-success rounded-circle"
													>
														<i class="bi bi-gear align-middle text-success fs-4" />
													</span>
												</span>

												<div class="flex-grow-1 flex-wrap pe-3">
													<span class="mb-0 d-block"
														><strong>Updated</strong> Your account password updated succuessfully</span
													>
													<small class="text-body-secondary">2h Ago</small>
												</div>
											</a>
										</li>
										<!--//Notification item start//-->
										<li class="list-group-item">
											<a
												href="#"
												class="list-group-item-action px-3 py-2 text-reset d-flex align-items-center"
											>
												<span class="d-block me-3">
													<span
														class="d-flex align-items-center justify-content-center lh-1 size-50 bg-danger-subtle text-danger rounded-circle"
													>
														<i class="bi bi-percent align-middle text-danger fs-4" />
													</span>
												</span>

												<div class="flex-grow-1 flex-wrap pe-3">
													<span class="mb-0 d-block"
														><strong>Pro discount</strong> Upgrade to pro plan with 30% discount,
														Apply coupon <span class="badge bg-primary">PRO30</span></span
													>
													<small class="text-body-secondary">2h Ago</small>
												</div>
											</a>
										</li>
									</ul>
								</div>
							</div>
						</div>
						<!-- -->
						<div class="col-lg-6 mb-3 mb-lg-5">
							<div class="card">
								<div class="card-header d-flex align-items-center justify-content-between">
									<h5 class="mb-0 me-3">Recent Activity</h5>
									<a href="#!">View All</a>
								</div>
								<div class="card-body">
									<ul class="step list-unstyled mb-0">
										<li class="step-item">
											<div class="step-row">
												<span class="step-icon">
													<!--Avatar-->
													<span
														class="avatar sm avatar-status status-online rounded-circle d-flex align-items-center justify-content-center bg-primary text-white"
													>
														<b>R</b>
													</span>
												</span>

												<div class="step-content">
													<h6 class="mb-1">Raymond Atkins</h6>
													<span class="lh-sm d-block mb-1"
														>Added <a href="#!">Felipe Grace</a> to project group</span
													>
													<small class="d-block mb-0 text-body-secondary">3h ago</small>
												</div>
											</div>
										</li>
										<!--/.step-item-->
										<li class="step-item">
											<div class="step-row">
												<span class="step-icon">
													<!--Avatar-->
													<span class="avatar sm avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</span>
												</span>

												<div class="step-content">
													<h6 class="mb-1">Abdul Kadir</h6>
													<span class="lh-sm d-block mb-1"
														>Created a new task <a href="#!">#235</a></span
													>
													<small class="d-block mb-0 text-body-secondary">3h ago</small>
												</div>
											</div>
										</li>
										<!--/.step-item-->
										<li class="step-item">
											<div class="step-row">
												<span class="step-icon">
													<!--Avatar-->
													<span class="avatar sm avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</span>
												</span>

												<div class="step-content">
													<h6 class="mb-1">Jessica</h6>
													<span class="d-block mb-2 lh-sm small">Added CSS file</span>
													<!--Post-->
													<div class="p-3 border rounded-3 mb-1 d-flex align-items-center">
														<i class="bi bi-filetype-css fs-1 mx-3" />
														<div class="flex-grow-1 overflow-hidden">
															<p class="mb-1 lh-sm text-truncate">tooltip-popover.css</p>
															<div class="d-flex align-items-center justify-content-between">
																<small class="text-body-secondary">4KB</small>
																<a href="#!" class="text-body">
																	<i class="bi bi-download align-middle text-success fs-5" />
																</a>
															</div>
														</div>
													</div>
													<small class="d-block text-body-secondary">Sep 14, 12:24PM EST</small>
												</div>
											</div>
										</li>
										<!--/.step-item-->

										<!--.step-item-->
										<li class="step-item">
											<div class="step-row">
												<span class="step-icon">
													<!--Avatar-->
													<span class="avatar sm avatar-status status-online">
														<img
															src={sample_image_3}
															class="img-fluid rounded-circle w-auto"
															alt=""
														/>
													</span>
												</span>

												<div class="step-content">
													<h6 class="mb-1">Adam Voes</h6>
													<span class="lh-sm d-block mb-1"
														>Reassigned a tasked to <a href="#!">Jessica</a>
														<a href="#!">#078</a></span
													>
													<small class="d-block mb-0 text-body-secondary"
														>June 14, 12:24PM EST</small
													>
												</div>
											</div>
										</li>
										<!--/.step-item-->
									</ul>
								</div>
							</div>
						</div>
						<!-- -->
						<!-- -->
						<!-- -->
						<!-- -->
						<!-- -->
						<!-- -->
					</div>

					<div class=" px-0">
						<div class="d-flex mb-7 align-items-center">
							<div class="flex-grow-1 border-top border-gray" />
							<h5 class="flex-shrink-0 mb-0 px-3">Other Widgets</h5>
							<div class="flex-grow-1 border-top border-gray" />
						</div>
						<div class="row mb-5">
							<!-- -->
							<div class="col-xl-7 mb-3 mb-lg-5">
								<!--card-->
								<div class="card table-nowrap table-card overflow-hidden h-100">
									<div class="d-flex card-header justify-content-between">
										<h5 class="me-3 card-title mb-0">Top Products</h5>
										<a href="#!.html">View All</a>
									</div>
									<div class="table-responsive">
										<table class="table mb-0" style="width:100%">
											<thead class="text-body-secondary text-uppercase small bg-body">
												<tr>
													<th class="ps-3" style="width:190px">Product</th>
													<th>Change</th>
													<th>Price</th>
													<th>Sold</th>
													<th class="text-end">Sales</th>
												</tr>
											</thead>
											<tbody class="align-middle">
												<tr>
													<td>
														<div class="d-flex align-items-center">
															<a href="#!.html"
																><img
																	src={sample_image_4}
																	class="avatar p-1 border rounded-2 me-2 align-middle"
																	alt=""
																/></a
															>
															<p class="mb-0 text-truncate">
																<a href="#!.html" class="text-reset"
																	>Apple white earbuds water proof</a
																>
															</p>
														</div>
													</td>
													<td>
														<div class="d-flex align-items-center">
															<span class="me-2">8%</span>
															<span class="small text-success">
																<i class="bi bi-arrow-up-right align-middle text-success fs-5" />
															</span>
														</div>
													</td>
													<td>$69</td>
													<td>9040</td>
													<td class="text-end">$623,760</td>
												</tr>
												<tr>
													<td class="">
														<div class="d-flex align-items-center">
															<a href="#!.html"
																><img
																	src={sample_image_4}
																	class="avatar p-1 border rounded-2 me-2 align-middle"
																	alt=""
																/></a
															>
															<p class="mb-0 text-truncate">
																<a href="#!.html" class="text-reset">Mini handbag for woomens</a>
															</p>
														</div>
													</td>
													<td>
														<div class="d-flex align-items-center">
															<span class="me-2">6%</span>
															<span class="small text-success">
																<i class="bi bi-arrow-up-right align-middle text-success fs-5" />
															</span>
														</div>
													</td>
													<td>$59</td>
													<td>8475</td>
													<td class="text-end">$500,025</td>
												</tr>
												<tr>
													<td class="">
														<div class="d-flex align-items-center">
															<a href="#!.html"
																><img
																	src={sample_image_4}
																	class="avatar p-1 border rounded-2 me-2 align-middle"
																	alt=""
																/></a
															>
															<p class="mb-0 text-truncate">
																<a href="#!.html" class="text-reset"
																	>Minimalist wireless headphone</a
																>
															</p>
														</div>
													</td>
													<td>
														<div class="d-flex align-items-center">
															<span class="me-2">11%</span>
															<span class="small text-success">
																<i class="bi bi-arrow-up-right align-middle text-success fs-5" />
															</span>
														</div>
													</td>
													<td>$59</td>
													<td>7321</td>
													<td class="text-end">$431,939</td>
												</tr>
												<tr>
													<td class="">
														<div class="d-flex align-items-center">
															<a href="#!.html"
																><img
																	src={sample_image_4}
																	class="avatar p-1 border rounded-2 me-2 align-middle"
																	alt=""
																/></a
															>
															<p class="mb-0 text-truncate">
																<a href="#!.html" class="text-reset">Google home mini</a>
															</p>
														</div>
													</td>
													<td>
														<div class="d-flex align-items-center">
															<span class="me-2">-7%</span>
															<span class="small text-danger">
																<i class="bi bi-arrow-down-right align-middle text-danger fs-5" />
															</span>
														</div>
													</td>
													<td>$39</td>
													<td>5485</td>
													<td class="text-end">$212,862</td>
												</tr>
											</tbody>
										</table>
									</div>
								</div>
							</div>
							<!-- -->
							<div class="col-xl-5 mb-3 mb-lg-5">
								<div class="card h-100">
									<div class="d-flex card-header justify-content-between">
										<h5 class="me-3 mb-0">Top Users by Country</h5>
										<a href="#!.html">View All</a>
									</div>
									<div class="card-body">
										<ul class="list-group list-group-flush">
											<!--List-item-->
											<li class="list-group-item pt-0">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_us} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">United States</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 31%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_uk} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">United Kingdom</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 24%</span
														>
													</div>
												</div>
											</li>

											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_poland} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">Poland</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 20%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_spain} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">Spain</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-down-fill align-middle text-danger" />
															7%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_kenya} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">Kenya</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 6%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_korea} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">Korea</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 5.5%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_france} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">France</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 3.5%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_china} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">China</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-down-fill align-middle text-danger" /> 1.75%</span
														>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0">
														<img src={flag_vietnam} alt="" class="width-20 rounded-1 h-auto" />
													</div>
													<div class="flex-grow-1 px-2">Vietnam</div>
													<div class="flex-shrink-0">
														<span>
															<i class="bi bi-caret-up-fill align-middle text-success" /> 1.25%</span
														>
													</div>
												</div>
											</li>
										</ul>
									</div>
								</div>
							</div>

							<!-- -->
							<div class="col-xl-5 mb-3 mb-lg-5">
								<div class="card">
									<div class="d-flex card-header justify-content-between">
										<h5 class="me-3 mb-0">Top Customers</h5>
										<a href="#!.html">View All</a>
									</div>
									<div class="card-body">
										<ul class="list-group list-group-flush">
											<!--List-item-->
											<li class="list-group-item pt-0">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0 me-3">
														<img src={sample_image_3} alt="" class="avatar rounded-circle" />
													</div>
													<div class="flex-grow-1">
														<h6 class="mb-0">Inara Britt</h6>
														<p class="mb-0 text-body-secondary">Georgia, USA</p>
													</div>
													<div class="flex-shrink-0 text-end">
														<span> $927.00 </span>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0 me-3">
														<img src={sample_image_3} alt="" class="avatar rounded-circle" />
													</div>
													<div class="flex-grow-1">
														<h6 class="mb-0">Eduard Franz</h6>
														<p class="mb-0 text-body-secondary">London, UK</p>
													</div>
													<div class="flex-shrink-0 text-end">
														<span> $916.00 </span>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0 me-3">
														<img src={sample_image_3} alt="" class="avatar rounded-circle" />
													</div>
													<div class="flex-grow-1">
														<h6 class="mb-0">Gianluca Darby</h6>
														<p class="mb-0 text-body-secondary">São Paulo, Brazil</p>
													</div>
													<div class="flex-shrink-0 text-end">
														<span> $896.50 </span>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0 me-3">
														<img src={sample_image_3} alt="" class="avatar rounded-circle" />
													</div>
													<div class="flex-grow-1">
														<h6 class="mb-0">Milana Myles</h6>
														<p class="mb-0 text-body-secondary">Marseille, France</p>
													</div>
													<div class="flex-shrink-0 text-end">
														<span> $874.50 </span>
													</div>
												</div>
											</li>
											<!--List-item-->
											<li class="list-group-item pb-0">
												<div class="d-flex align-items-center">
													<div class="flex-shrink-0 me-3">
														<img src={sample_image_3} alt="" class="avatar rounded-circle" />
													</div>
													<div class="flex-grow-1">
														<h6 class="mb-0">Taisiia Oluchi</h6>
														<p class="mb-0 text-body-secondary">Durban, SA</p>
													</div>
													<div class="flex-shrink-0 text-end">
														<span> $857.50 </span>
													</div>
												</div>
											</li>
										</ul>
									</div>
								</div>
							</div>

							<!-- -->
							<div class="col-12 mb-3 mb-lg-5">
								<div class="overflow-hidden card table-nowrap table-card">
									<div class="card-header d-flex justify-content-between align-items-center">
										<h5 class="mb-0">New customers</h5>
										<a href="#!" class="btn btn-outline-secondary btn-sm">View All</a>
									</div>
									<div class="table-responsive">
										<table class="table mb-0">
											<thead class="small text-uppercase bg-body text-body-secondary">
												<tr>
													<th>Name</th>
													<th>Email</th>
													<th>Country</th>
													<th>Payment method</th>
													<th>Created Date</th>
													<th class="text-end">Action</th>
												</tr>
											</thead>
											<tbody>
												<tr class="align-middle">
													<td>
														<div class="d-flex align-items-center">
															<img
																src={sample_image_3}
																class="avatar sm rounded-pill me-3 flex-shrink-0"
																alt="Customer"
															/>
															<div>
																<div class="h6 mb-0 lh-1">Mark Voldov</div>
															</div>
														</div>
													</td>
													<td>mvoges@email.com</td>
													<td
														><img
															src={flag_korea}
															class="width-20 h-auto me-2 rounded-pill align-middle"
															alt=""
														/> <span class="d-inline-block align-middle">Korea</span></td
													>
													<td><span>****6231</span></td>
													<td>21 Sep, 2023</td>
													<td class="text-end">
														<div class="drodown">
															<a
																data-bs-toggle="dropdown"
																href="#"
																class="btn btn-outline-secondary p-1"
															>
																<i class="bi bi-three-dots-vertical" />
															</a>
															<div class="dropdown-menu dropdown-menu-end">
																<a href="#!" class="dropdown-item">View Details</a>
																<a href="#!" class="dropdown-item">Delete user</a>
															</div>
														</div>
													</td>
												</tr>
												<tr class="align-middle">
													<td>
														<div class="d-flex align-items-center">
															<img
																src={sample_image_3}
																class="avatar sm rounded-pill me-3 flex-shrink-0"
																alt="Customer"
															/>
															<div>
																<div class="h6 mb-0 lh-1">Topias Kantola</div>
															</div>
														</div>
													</td>
													<td>topiaskantola@email.com</td>
													<td
														><img
															src={flag_korea}
															class="width-20 h-auto me-2 rounded-pill align-middle"
															alt=""
														/> <span class="d-inline-block align-middle">Korea</span></td
													>
													<td><span>****@mail.com</span></td>
													<td>21 Sep, 2023</td>
													<td class="text-end">
														<div class="drodown">
															<a
																data-bs-toggle="dropdown"
																href="#"
																class="btn btn-outline-secondary p-1"
															>
																<i class="bi bi-three-dots-vertical" />
															</a>
															<div class="dropdown-menu dropdown-menu-end">
																<a href="#!" class="dropdown-item">View Details</a>
																<a href="#!" class="dropdown-item">Delete user</a>
															</div>
														</div>
													</td>
												</tr>
												<tr class="align-middle">
													<td>
														<div class="d-flex align-items-center">
															<img
																src={sample_image_3}
																class="avatar sm rounded-pill me-3 flex-shrink-0"
																alt="Customer"
															/>
															<div>
																<div class="h6 mb-0 lh-1">Anaiah Whitten</div>
															</div>
														</div>
													</td>
													<td>anaiahwhitten@email.com</td>
													<td
														><img
															src={flag_korea}
															class="width-20 h-auto me-2 rounded-pill align-middle"
															alt=""
														/>
														<span class="d-inline-block align-middle">Korea</span>
													</td>
													<td><span>****0014</span></td>
													<td>12 June, 2022</td>
													<td class="text-end">
														<div class="drodown">
															<a
																data-bs-toggle="dropdown"
																href="#"
																class="btn btn-outline-secondary p-1"
															>
																<i class="bi bi-three-dots-vertical" />
															</a>
															<div class="dropdown-menu dropdown-menu-end">
																<a href="#!" class="dropdown-item">View Details</a>
																<a href="#!" class="dropdown-item">Delete user</a>
															</div>
														</div>
													</td>
												</tr>
												<tr class="align-middle">
													<td>
														<div class="d-flex align-items-center">
															<img
																src={sample_image_3}
																class="avatar sm rounded-pill me-3 flex-shrink-0"
																alt="Customer"
															/>
															<div>
																<div class="h6 mb-0 lh-1">Wyatt Morris</div>
															</div>
														</div>
													</td>
													<td>wyattmorris@email.com</td>
													<td
														><img
															src={flag_korea}
															class="width-20 h-auto me-2 rounded-pill align-middle"
															alt=""
														/>
														<span class="d-inline-block align-middle">Korea</span>
													</td>
													<td><span>****8715</span></td>
													<td>04 June, 2022</td>
													<td class="text-end">
														<div class="drodown">
															<a
																data-bs-toggle="dropdown"
																href="#"
																class="btn btn-outline-secondary p-1"
															>
																<i class="bi bi-three-dots-vertical" />
															</a>
															<div class="dropdown-menu dropdown-menu-end">
																<a href="#!" class="dropdown-item">View Details</a>
																<a href="#!" class="dropdown-item">Delete user</a>
															</div>
														</div>
													</td>
												</tr>
												<tr class="align-middle">
													<td>
														<div class="d-flex align-items-center">
															<img
																src={sample_image_3}
																class="avatar sm rounded-pill me-3 flex-shrink-0"
																alt="Customer"
															/>
															<div>
																<div class="h6 mb-0 lh-1">Eliana Stout</div>
															</div>
														</div>
													</td>
													<td>elianastout@email.com</td>
													<td
														><img
															src={flag_korea}
															class="width-20 h-auto me-2 rounded-pill align-middle"
															alt=""
														/>
														<span class="d-inline-block align-middle">Korea</span>
													</td>
													<td><span>****1010</span></td>
													<td>01 April, 2022</td>
													<td class="text-end">
														<div class="drodown">
															<a
																data-bs-toggle="dropdown"
																href="#"
																class="btn btn-outline-secondary p-1"
															>
																<i class="bi bi-three-dots-vertical" />
															</a>
															<div class="dropdown-menu dropdown-menu-end">
																<a href="#!" class="dropdown-item">View Details</a>
																<a href="#!" class="dropdown-item">Delete user</a>
															</div>
														</div>
													</td>
												</tr>
											</tbody>
										</table>
									</div>
								</div>
							</div>

							<!-- -->
							<div class="col-12 mb-3 mb-lg-5">
								<div class="position-relative card table-nowrap table-card">
									<div class="card-header align-items-center">
										<h5 class="mb-0">Latest Transactions</h5>
										<p class="mb-0 small text-body-secondary">1 Pending</p>
									</div>
									<div class="table-responsive">
										<table class="table mb-0">
											<thead class="small text-uppercase bg-body text-body-secondary">
												<tr>
													<th>Transaction ID</th>
													<th>Date</th>
													<th>Name</th>
													<th>Amount</th>
													<th>Status</th>
												</tr>
											</thead>
											<tbody>
												<tr class="align-middle">
													<td> #57473829 </td>
													<td>13 Sep, 2021</td>
													<td>Renee Sims</td>
													<td>
														<div class="d-flex align-items-center">
															<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-danger" />
															<span>$145</span>
														</div>
													</td>
													<td>
														<span class="badge bg-success-subtle text-success">Completed</span>
													</td>
												</tr>
												<tr class="align-middle">
													<td> #012458780 </td>
													<td>19 Aug, 2021</td>
													<td>Edith Koenig</td>
													<td>
														<div class="d-flex align-items-center">
															<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-danger" />

															<span>$641.64</span>
														</div>
													</td>
													<td>
														<span class="badge bg-warning-subtle text-warning">Pending</span>
													</td>
												</tr>
												<tr class="align-middle">
													<td> #76444326 </td>
													<td>03 April, 2021</td>
													<td>Carrie Blount</td>
													<td>
														<div class="d-flex align-items-center">
															<i
																class="bi bi-caret-down-fill align-middle fs-5 me-1 text-success"
															/>

															<span>$12,457</span>
														</div>
													</td>
													<td>
														<span class="badge bg-success-subtle text-success">Completed</span>
													</td>
												</tr>
												<tr class="align-middle">
													<td> #12498745 </td>
													<td>15 March, 2021</td>
													<td>Ander Durham</td>
													<td>
														<div class="d-flex align-items-center">
															<i
																class="bi bi-caret-down-fill align-middle fs-5 me-1 text-success"
															/>
															<span>$785</span>
														</div>
													</td>
													<td>
														<span class="badge bg-success-subtle text-success">Completed</span>
													</td>
												</tr>
												<tr class="align-middle">
													<td> #87444654 </td>
													<td>23 Jan, 2021</td>
													<td>Netflix Inc.</td>
													<td>
														<div class="d-flex align-items-center">
															<i class="bi bi-caret-up-fill align-middle fs-5 me-1 text-danger" />

															<span>$199</span>
														</div>
													</td>
													<td>
														<span class="badge bg-success-subtle text-success">Completed</span>
													</td>
												</tr>
											</tbody>
										</table>
									</div>
									<div class="card-footer text-end">
										<a href="#!" class="btn btn-sm btn-secondary">View All Transactions</a>
									</div>
								</div>
							</div>

							<!-- -->
						</div>

						<!--Widget row Title-->
						<div class="d-flex mb-7 align-items-center">
							<div class="flex-grow-1 border-top border-gray" />

							<h5 class="flex-shrink-0 mb-0 px-3">Recently Added Widgets</h5>
							<div class="flex-grow-1 border-top border-gray" />
						</div>

						<div class="row">
							<div class="col-12 col-xl-6 mb-3 mb-lg-5">
								<div class="card overflow-hidden h-100">
									<div class="card-header d-flex align-items-center">
										<h5 class="mb-0 flex-grow-1 text-truncate pe-3">Bandwidth Summary</h5>
										<a href="#!" class="flex-shrink-0 btn btn-sm btn-outline-secondary">
											<i class="bi bi-download align-middle fs-5 me-1" />
											Download Report</a
										>
									</div>
									<div class="card-body p-0">
										<div class="row mx-0">
											<div class="col-sm-6 col-12 p-4 border-bottom border-end-sm">
												<!--::begin bandwidth card-->
												<div class="position-relative">
													<div class="position-relative">
														<div class="d-flex align-items-center justify-content-between">
															<div>
																<span class="fs-4 fw-bold">393</span>
																<span class="small">Mb</span>
															</div>
															<p class="mb-0">HTTP Traffic</p>
														</div>
														<!--Progress bar-->
														<div class="progress my-2 height-5">
															<div
																class="progress-bar rounded-pill progress-bar-striped progress-bar-animated"
																role="progressbar"
																aria-label="Animated striped example"
																style="width: 17%"
															/>
														</div>
														<div class="d-flex align-items-center justify-content-between">
															<p class="mb-0 small">Monthly target</p>
															<p class="mb-0 small">17%</p>
														</div>
													</div>
												</div>
												<!--::/.end bandwidth card-->
											</div>
											<div class="col-sm-6 col-12 p-4 border-bottom">
												<!--::begin bandwidth card-->
												<div class="position-relative">
													<div class="position-relative">
														<div class="d-flex align-items-center justify-content-between">
															<div>
																<span class="fs-4 fw-bold">151</span>
																<span class="small">Mb</span>
															</div>
															<p class="mb-0">SMTP Traffic</p>
														</div>
														<!--Progress bar-->
														<div class="progress my-2 height-5">
															<div
																class="progress-bar bg-warning rounded-pill progress-bar-striped progress-bar-animated"
																role="progressbar"
																aria-label="Animated striped example"
																style="width: 34%"
															/>
														</div>
														<div class="d-flex align-items-center justify-content-between">
															<p class="mb-0 small">Monthly target</p>
															<p class="mb-0 small">34%</p>
														</div>
													</div>
												</div>
												<!--::/.end bandwidth card-->
											</div>
											<div
												class="col-sm-6 col-12 p-4 border-end-sm border-bottom border-bottom-sm-0"
											>
												<!--::begin bandwidth card-->
												<div class="position-relative">
													<div class="position-relative">
														<div class="d-flex align-items-center justify-content-between">
															<div>
																<span class="fs-4 fw-bold">247</span>
																<span class="small">Mb</span>
															</div>
															<p class="mb-0">FTP Traffic</p>
														</div>
														<!--Progress bar-->
														<div class="progress my-2 height-5">
															<div
																class="progress-bar rounded-pill bg-success progress-bar-striped progress-bar-animated"
																role="progressbar"
																aria-label="Animated striped example"
																style="width: 21%"
															/>
														</div>
														<div class="d-flex align-items-center justify-content-between">
															<p class="mb-0 small">Monthly target</p>
															<p class="mb-0 small">21%</p>
														</div>
													</div>
												</div>
												<!--::/.end bandwidth card-->
											</div>
											<div class="col-sm-6 col-12 p-4">
												<!--::begin bandwidth card-->
												<div class="position-relative">
													<div class="position-relative">
														<div class="d-flex align-items-center justify-content-between">
															<div>
																<span class="fs-4 fw-bold">27</span>
																<span class="small">Mb</span>
															</div>
															<p class="mb-0">POP3 Traffic</p>
														</div>
														<!--Progress bar-->
														<div class="progress my-2 height-5">
															<div
																class="progress-bar rounded-pill bg-danger progress-bar-striped progress-bar-animated"
																role="progressbar"
																aria-label="Animated striped example"
																style="width: 18%"
															/>
														</div>
														<div class="d-flex align-items-center justify-content-between">
															<p class="mb-0 small">Monthly target</p>
															<p class="mb-0 small">18%</p>
														</div>
													</div>
												</div>
												<!--::/.end bandwidth card-->
											</div>
										</div>
										<div class="p-4 border-top-sm bg-body-tertiary">
											<div class="row align-items-center">
												<div class="col">
													<h5 class="text-danger">Running out of your space?</h5>
													<p>
														Your storage will be running out soon. Get more space and powerful
														productivity features.
													</p>
													<a href="#!" class="btn btn-primary btn-sm">Upgrade to Pro</a>
												</div>
												<div class="col-auto">
													<img src={sample_image_3} class="width-120 h-auto" alt="" />
												</div>
											</div>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>

					useful_cards.svelte
					<UsefulCards />

					project_stats.svelte
					<ProjectStats />

					chart_revenue_report.svelte
					<ChartRevenueReport />

					active_users_by_device.svelte
					<ActiveUsersByDevice />

					double_line_graph.svelte
					<DoubleLineGraph />

					double_bar_graph.svelte
					<DoubleBarGraph />
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
					<!-- -->
				</div>
			</div>
		</div>
	</div>
</div>
