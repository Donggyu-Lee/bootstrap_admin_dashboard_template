<script>
	import { onMount } from 'svelte';
</script>

<section class="position-relative">
	<!--:Pattern:-->
	<div
		class="bg-pattern text-primary text-opacity-50 opacity-25 w-100 vh-100 start-0 top-0 position-absolute"
	/>
	<div class="container pt-11 pt-lg-14 pb-9 pb-lg-11 position-relative z-1">
		<div class="row align-items-center justify-content-center">
			<div class="col-xl-4 col-lg-5 col-md-6 col-sm-8 z-2">
				<h2 class="mb-5 display-6 text-center">Bluekare-T <br /> Clinical Trial</h2>

				<div class="my-5">
					<ul class="nav nav-pills nav-fill mb-3" id="pills-tab" role="tablist">
						<li class="nav-item" role="presentation">
							<button
								class="nav-link active"
								id="pills-home-tab"
								data-bs-toggle="pill"
								data-bs-target="#pills-home"
								type="button"
								role="tab"
								aria-controls="pills-home"
								aria-selected="true">기관코드로 로그인</button
							>
						</li>
						<li class="nav-item" role="presentation">
							<button
								class="nav-link"
								id="pills-profile-tab"
								data-bs-toggle="pill"
								data-bs-target="#pills-profile"
								type="button"
								role="tab"
								aria-controls="pills-profile"
								aria-selected="false">ID/PW로 로그인</button
							>
						</li>
					</ul>
					<div class="tab-content" id="pills-tabContent">
						<div
							class="tab-pane fade show active"
							id="pills-home"
							role="tabpanel"
							aria-labelledby="pills-home-tab"
						>
							<form action="/?/code" method="POST">
								<div class="position-relative">
									<div>
										<div class="my-5 d-flex justify-content-center">
											<div class="form-check form-check-inline">
												<input
													class="form-check-input"
													type="radio"
													name="inlineRadioOptions"
													id="codedev"
													value="dev"
													required
												/>
												<label class="form-check-label" for="codedev">테스트 서버</label>
											</div>
											<div class="form-check form-check-inline">
												<input
													class="form-check-input"
													type="radio"
													name="inlineRadioOptions"
													id="codeaws"
													value="aws"
													checked
													required
												/>
												<label class="form-check-label" for="codeaws">임상 서버</label>
											</div>
										</div>

										<div class=" mb-3">
											<input
												name="organization"
												type="text"
												class="form-control text-center"
												required
												placeholder="기관 코드를 입력하세요"
											/>
										</div>

										<!-- <div class="mb-3 d-flex justify-content-end">
											<div>
												<label class="text-end d-block small mb-0"
													><a href="page-account-forget-password.html" class="link-decoration"
														>기관코드를 잊으셨나요?</a
													></label
												>
											</div>
										</div> -->

										<div class="d-grid">
											<button class="btn btn-success" type="submit"> 로그인 </button>
										</div>
									</div>
								</div>
							</form>
						</div>
						<div
							class="tab-pane fade"
							id="pills-profile"
							role="tabpanel"
							aria-labelledby="pills-profile-tab"
						>
							<form action="/?/idpw" method="POST">
								<div class="position-relative">
									<div>
										<div class="my-5 d-flex justify-content-center">
											<div class="form-check form-check-inline">
												<input
													class="form-check-input"
													type="radio"
													name="inlineRadioOptions"
													id="dev"
													value="dev"
													required
												/>
												<label class="form-check-label" for="dev">테스트 서버</label>
											</div>
											<div class="form-check form-check-inline">
												<input
													class="form-check-input"
													type="radio"
													name="inlineRadioOptions"
													id="aws"
													value="aws"
													required
													checked
												/>
												<label class="form-check-label" for="aws">임상 서버</label>
											</div>
										</div>
										<div class="row my-2 d-flex align-items-center">
											<div class="col-2">ID</div>
											<div class="col-10">
												<input
													name="id"
													type="text"
													class="form-control text-center"
													required
													placeholder="ID를 입력하세요"
												/>
											</div>
										</div>
										<div class="row my-2 d-flex align-items-center">
											<div class="col-2">PW</div>
											<div class="col-10">
												<input
													name="pw"
													type="password"
													class="form-control text-center"
													required
													placeholder="비밀번호를 입력하세요"
													autocomplete="on"
												/>
											</div>
										</div>

										<div class="d-grid my-2">
											<button class="btn btn-success" type="submit"> Sign in </button>
										</div>
									</div>
								</div>
							</form>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
