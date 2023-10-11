<script>
	import sample_image_1 from '$lib/images/AttnKare_logo.webp';
	import sample_image_2 from '$lib/images/BlueKare_logo.webp';
	import sample_image_3 from '$lib/images/profile_photo.jpeg';
	import sample_image_4 from '$lib/images/hippo_logo_icon_only.png';
</script>

<div class="row">
	<div class="col-12 mb-3 mb-lg-5">
		<div class="card table-card table-nowrap overflow-hidden">
			<div class="card-header d-flex align-items-center">
				<h5 class="mb-0 pe-3 flex-grow-1 text-truncate">Projects Stats</h5>
				<a href="#!" class="flex-shrink-0 btn btn-sm btn-outline-secondary">History</a>
			</div>
			<div class="table-responsive">
				<table class="table align-middle mb-0">
					<thead class="bg-body text-body-secondary small text-uppercase">
						<tr>
							<th>Project</th>
							<th class="text-end">Budget</th>
							<th class="text-end">Progress</th>
							<th class="text-end">Status</th>
							<th class="text-end">View</th>
						</tr>
					</thead>
					<tbody>
						<tr>
							<td>
								<div class="d-flex align-items-center">
									<div class="width-70 h-auto me-3">
										<img src={sample_image_1} class="img-fluid rounded" alt="" />
									</div>
									<div class="d-flex justify-content-start flex-column">
										<a href="#" class="h6 mb-1">IOS Health App</a>
										<span class="text-body-secondary d-block fs-6">Allie Grater</span>
									</div>
								</div>
							</td>
							<td class="text-end"><span class="text-body-secondary">$247,500</span></td>
							<td class="text-end">
								<div class="progress bg-danger-subtle height-5 rounded-pill">
									<div
										class="bg-danger rounded-pill progress-bar progress-bar-animated progress-bar-animated"
										style="width:24%"
									/>
								</div>
							</td>
							<td class="text-end">
								<span class="badge bg-success-subtle text-success"> Active</span>
							</td>
							<td class="text-end">
								<a href="#!" class="btn btn-outline-secondary btn-sm">
									<i class="bi bi-arrow-right fs-5" />
								</a>
							</td>
						</tr>
						<tr>
							<td>
								<div class="d-flex align-items-center">
									<div class="width-70 h-auto me-3">
										<img src={sample_image_1} class="img-fluid rounded" alt="" />
									</div>
									<div class="d-flex justify-content-start flex-column">
										<a href="#" class="h6 mb-1">Music Android App</a>
										<span class="text-body-secondary d-block fs-6">Lynn O’Leeum</span>
									</div>
								</div>
							</td>
							<td class="text-end"><span class="text-body-secondary">$66,500</span></td>
							<td class="text-end">
								<div class="progress bg-info-subtle height-5 rounded-pill">
									<div
										class="bg-info rounded-pill progress-bar progress-bar-animated progress-bar-animated"
										style="width:74%"
									/>
								</div>
							</td>
							<td class="text-end">
								<span class="badge bg-primary-subtle text-primary"> In Process</span>
							</td>
							<td class="text-end">
								<a href="#!" class="btn btn-outline-secondary btn-sm">
									<i class="bi bi-arrow-right fs-5" />
								</a>
							</td>
						</tr>
						<tr>
							<td>
								<div class="d-flex align-items-center">
									<div class="width-70 h-auto me-3">
										<img src={sample_image_2} class="img-fluid rounded" alt="" />
									</div>
									<div class="d-flex justify-content-start flex-column">
										<a href="#" class="h6 mb-1">Figma Landing</a>
										<span class="text-body-secondary d-block fs-6">Percy Vere</span>
									</div>
								</div>
							</td>
							<td class="text-end"><span class="text-body-secondary">$125,000</span></td>
							<td class="text-end">
								<div class="progress bg-primary-subtle height-5 rounded-pill">
									<div
										class="bg-primary rounded-pill progress-bar progress-bar-animated progress-bar-animated"
										style="width:84%"
									/>
								</div>
							</td>
							<td class="text-end">
								<span class="badge bg-warning-subtle text-warning"> On Hold</span>
							</td>
							<td class="text-end">
								<a href="#!" class="btn btn-outline-secondary btn-sm">
									<i class="bi bi-arrow-right fs-5" />
								</a>
							</td>
						</tr>
						<tr>
							<td>
								<div class="d-flex align-items-center">
									<div class="width-70 h-auto me-3">
										<img src={sample_image_2} class="img-fluid rounded" alt="" />
									</div>
									<div class="d-flex justify-content-start flex-column">
										<a href="#" class="h6 mb-1">Shopify Website</a>
										<span class="text-body-secondary d-block fs-6">Jack Aranda</span>
									</div>
								</div>
							</td>
							<td class="text-end"><span class="text-body-secondary">$85,000</span></td>
							<td class="text-end">
								<div class="progress bg-success-subtle height-5 rounded-pill">
									<div
										class="bg-success rounded-pill progress-bar progress-bar-animated progress-bar-animated"
										style="width:62%"
									/>
								</div>
							</td>
							<td class="text-end">
								<span class="badge bg-warning-subtle text-warning"> On Hold</span>
							</td>
							<td class="text-end">
								<a href="#!" class="btn btn-outline-secondary btn-sm">
									<i class="bi bi-arrow-right fs-5" />
								</a>
							</td>
						</tr>
					</tbody>
				</table>
			</div>
		</div>
	</div>
</div>
