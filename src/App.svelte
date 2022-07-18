<script>
	import PRELOAD from "./components/preload.svelte"
	import SECTONE from "./pages/section-one.svelte"
	import POPUP  from "./components/popup.svelte"

	$: navToggle = false;
	let popup = true

	const key = "BUTAO-MWS-POPUP"

	if(localStorage.getItem(key) != null){
		let pData = localStorage.getItem(key);
		popup = JSON.parse(pData)

	}

	function rMLater(){
		popup = false;
		localStorage.setItem(key, JSON.stringify(popup))
	}

	function nav(){
		navToggle = !navToggle
		console.log(navToggle)
	}



	
</script>

{#if popup === true}
<article class="popup">
	<p>{popup}</p>
	<POPUP on:popend={rMLater} />
</article>
{/if}
<div id="layout">
	<div class="lay">
		<div class="preload-sect">
			<PRELOAD />
		</div>
		<header>
		</header>
		<main>
			<section id="main-layout">
				<div class="mn-layout">
			
					<div class="navigation-top">
						<div class="nv-top">
			
							<nav>
							
								<div class="about">
									<p>
										<span>
											<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
												<path d="M3 12C3 13.1053 3.89474 14 5 14C6.10526 14 7 13.1053 7 12C7 10.8947 6.10526 10 5 10C3.89474 10 3 10.8947 3 12ZM10 12C10 13.1053 10.8947 14 12 14C13.1053 14 14 13.1053 14 12C14 10.8947 13.1053 10 12 10C10.8947 10 10 10.8947 10 12ZM17 12C17 13.1053 17.8947 14 19 14C20.1053 14 21 13.1053 21 12C21 10.8947 20.1053 10 19 10C17.8947 10 17 10.8947 17 12Z" fill="#0C99FF"/>
												</svg>
												
										</span>
									</p>
								</div>
								<div class="about-content">
									<div class="abt-cnt">
			
										<div class="title">
											<p>about maka story book</p>
											<p>
												<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="64" height="20" viewBox="0 0 64 20"><defs><filter id="a" x="6" y="0" width="52" height="20" filterUnits="userSpaceOnUse"><feOffset dy="3" input="SourceAlpha"/><feGaussianBlur stdDeviation="3" result="b"/><feFlood flood-color="#ed1e79"/><feComposite operator="in" in2="b"/><feComposite in="SourceGraphic"/></filter><filter id="c" x="44" y="0" width="20" height="20" filterUnits="userSpaceOnUse"><feOffset dy="3" input="SourceAlpha"/><feGaussianBlur stdDeviation="3" result="d"/><feFlood flood-color="#ed1e79"/><feComposite operator="in" in2="d"/><feComposite in="SourceGraphic"/></filter></defs><g transform="translate(-296 -108)"><g transform="matrix(1, 0, 0, 1, 296, 108)" filter="url(#a)"><rect width="34" height="2" transform="translate(15 6)" fill="#ed1e79"/></g><rect width="2" height="2" transform="translate(306 114)" fill="#63c5cd"/><rect width="2" height="2" transform="translate(296 114)" fill="#63c5cd"/><rect width="2" height="2" transform="translate(346 114)" fill="#63c5cd"/><g transform="matrix(1, 0, 0, 1, 296, 108)" filter="url(#c)"><rect width="2" height="2" transform="translate(53 6)" fill="#ed1e79"/></g></g></svg>
											</p>
										</div>
			
										<div class="logo">
											<div class="svg-logo">logo</div>
										</div>
			
										<div class="version">
											<p>version : 1.1.1</p>
										</div>
			
										<div class="readme">
											<div class="title">
												<h1>READ ME</h1>
											</div>
											<div class="paragraphs">
												<div class="para">
													<h1>what is maka animation story books</h1>
													<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta illo vero ducimus doloribus quibusdam alias accusantium repudiandae aspernatur nesciunt facere nisi corporis earum obcaecati perferendis dolorum similique ullam, illum officia aperiam aut est voluptatum quos tenetur cupiditate. Aliquid amet dignissimos magnam enim sit autem fugit, quibusdam corrupti eius ut numquam.</p>
												</div>
												<div class="para">
													<h1>why you should get involved</h1>
													<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officia voluptatibus doloribus voluptatem optio distinctio placeat exercitationem vero a molestias minus, natus numquam rerum at. Illum dolorem recusandae voluptatem, voluptatibus fugit expedita quam molestias, facere natus, quaerat tenetur cum nulla eum in. Explicabo quo ipsum similique aliquam assumenda voluptatibus ut. Earum.</p>
												</div>
											</div>
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="64" height="20" viewBox="0 0 64 20"><defs><filter id="a" x="6" y="0" width="52" height="20" filterUnits="userSpaceOnUse"><feOffset dy="3" input="SourceAlpha"/><feGaussianBlur stdDeviation="3" result="b"/><feFlood flood-color="#ed1e79"/><feComposite operator="in" in2="b"/><feComposite in="SourceGraphic"/></filter><filter id="c" x="44" y="0" width="20" height="20" filterUnits="userSpaceOnUse"><feOffset dy="3" input="SourceAlpha"/><feGaussianBlur stdDeviation="3" result="d"/><feFlood flood-color="#ed1e79"/><feComposite operator="in" in2="d"/><feComposite in="SourceGraphic"/></filter></defs><g transform="translate(-296 -108)"><g transform="matrix(1, 0, 0, 1, 296, 108)" filter="url(#a)"><rect width="34" height="2" transform="translate(15 6)" fill="#ed1e79"/></g><rect width="2" height="2" transform="translate(306 114)" fill="#63c5cd"/><rect width="2" height="2" transform="translate(296 114)" fill="#63c5cd"/><rect width="2" height="2" transform="translate(346 114)" fill="#63c5cd"/><g transform="matrix(1, 0, 0, 1, 296, 108)" filter="url(#c)"><rect width="2" height="2" transform="translate(53 6)" fill="#ed1e79"/></g></g></svg>
										</div>
										<div class="footer">
											<footer>
												<div class="ft">
													<div class="butao-logo">
														logo
													</div>
													<div class="copy">
														<p>
															copyright © makaanimationsstudio 2022
														</p>
													</div>
													<div class="author">
														<article>
															<a href="http://butaopeter.netlify.app">BUTAO UX/UI DEV</a>
														</article>
													</div>
												</div>
											</footer>
										</div>
			
									</div>
								</div>
							</nav>
			
						</div>
					</div>
					<div class="content">
						<div class="container">
							<div class="section-one">
								<div class="so">
									<SECTONE />
								</div>
							</div>
							
						</div>
					</div>
					<div class="navigation-bottom">
						<div class="nv-bottom">
							<nav>
								<ul>
									<li>
										<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
											<path d="M15 14.0031C15 12.3365 13.6667 11.0031 12 11.0031C10.3333 11.0031 9 12.3365 9 14.0031V19.0031H7C5.77193 19.0031 5 18.2312 5 17.0031V11.2488C5 10.6347 5.15789 10.2488 5.57895 9.82771L10.5789 4.82771C11.4737 3.95052 12.5263 3.95052 13.4211 4.82771L18.4211 9.82771C18.8421 10.2488 19 10.6347 19 11.2488V17.0031C19 18.2312 18.2281 19.0031 17 19.0031H15V14.0031ZM13 14.0031V21.0031H17C19.2105 21.0031 21 19.2137 21 17.0031V11.2488C21 10.1786 20.5789 9.16104 19.8246 8.4242L14.8246 3.4242C13.2632 1.84525 10.7368 1.84525 9.17544 3.4242L4.17544 8.4242C3.42105 9.16104 3 10.1786 3 11.2488V17.0031C3 19.2137 4.78947 21.0031 7 21.0031H11V14.0031C11 13.3189 11.3158 13.0031 12 13.0031C12.6842 13.0031 13 13.3189 13 14.0031ZM14 19.0031H10V21.0031H14V19.0031Z" fill="#E69C31"/>
											</svg>
											
									
									</li>
									<li>
										<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
											<path d="M11 12C11 14.2632 10.5614 16.4035 9.70175 18.5088C9.45614 19.0877 9.17544 19.6667 8.87719 20.2456C8.78947 20.386 8.75439 20.5439 8.75439 20.7193C8.75439 21.2632 9.21053 21.7193 9.75439 21.7193C10.1404 21.7193 10.4737 21.5088 10.6316 21.193C10.9649 20.5789 11.2807 19.9298 11.5614 19.2807C12.4912 16.9649 13 14.4912 13 12C13 11.4561 12.5439 11 12 11C11.4561 11 11 11.4561 11 12ZM13.9123 21.3684C14.0351 21.0702 14.193 20.7544 14.3333 20.4035C15.4211 17.7544 16 14.8772 16 12C16 9.78947 14.2105 8 12 8C9.78947 8 8 9.78947 8 12C8 13.8596 7.64912 15.614 6.92982 17.3509C6.70175 17.9123 6.4386 18.4561 6.12281 19C6.05263 19.1404 6 19.3158 6 19.4912C6 20.0351 6.45614 20.4912 7 20.4912C7.36842 20.4912 7.70175 20.2807 7.87719 19.9825C8.19298 19.4035 8.52632 18.7544 8.78947 18.1228C9.57895 16.1754 10 14.0877 10 12C10 10.7719 10.7719 10 12 10C13.2281 10 14 10.7719 14 12C14 14.6667 13.4912 17.2105 12.4737 19.6667C12.3684 19.9474 12.2456 20.2281 12.0877 20.5263C12.0351 20.6491 12 20.7895 12 20.9474C12 21.4912 12.4561 21.9474 13 21.9474C13.4035 21.9474 13.7368 21.7193 13.9123 21.3684ZM22 12C22 6.47368 17.5263 2 12 2C6.47368 2 2 6.47368 2 12C2 12.5439 2.45614 13 3 13C3.54386 13 4 12.5439 4 12C4 7.45614 7.45614 4 12 4C16.5439 4 20 7.45614 20 12C20 12.5439 20.4561 13 21 13C21.5439 13 22 12.5439 22 12ZM17.7018 19.9649C18.5614 17.4211 19 14.6842 19 12C19 8.12281 15.8772 5 12 5C8.12281 5 5 8.12281 5 12C5 13.4737 4.7193 14.8421 4.15789 16.2105C4.07018 16.4561 3.96491 16.6667 3.85965 16.8947C3.78947 17.0175 3.75439 17.1754 3.75439 17.3333C3.75439 17.8772 4.21053 18.3333 4.75439 18.3333C5.14035 18.3333 5.49123 18.1053 5.64912 17.7719C5.78947 17.5088 5.89474 17.2281 6.01754 16.9825C6.64912 15.4035 7 13.7018 7 12C7 9.10526 9.10526 7 12 7C14.8947 7 17 9.10526 17 12C17 14.5088 16.5965 16.9474 15.807 19.3333C15.7719 19.4386 15.7544 19.5439 15.7544 19.6491C15.7544 20.193 16.2105 20.6491 16.7544 20.6491C17.193 20.6491 17.5614 20.3684 17.7018 19.9649Z" fill="#E69C31"/>
											</svg>
											
									</li>
									<li>
										<svg width="111" height="49" viewBox="0 0 111 49" fill="none" xmlns="http://www.w3.org/2000/svg">
											<g filter="url(#filter0_d_102_172)">
											<path d="M6 11C6 7.68629 8.68629 5 12 5H99C102.314 5 105 7.68629 105 11V36C105 39.3137 102.314 42 99 42H12C8.68629 42 6 39.3137 6 36V11Z" fill="#E69C31" fill-opacity="0.26" shape-rendering="crispEdges"/>
											</g>
											<path d="M64 20H57V13C57 12.4561 56.5439 12 56 12C55.4561 12 55 12.4561 55 13V22H64C64.5439 22 65 21.5439 65 21C65 20.4561 64.5439 20 64 20ZM48 22H55V29C55 29.5439 55.4561 30 56 30C56.5439 30 57 29.5439 57 29V20H48C47.4561 20 47 20.4561 47 21C47 21.5439 47.4561 22 48 22Z" fill="#E69C31"/>
											<defs>
											<filter id="filter0_d_102_172" x="0" y="0" width="111" height="49" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
											<feFlood flood-opacity="0" result="BackgroundImageFix"/>
											<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
											<feOffset dy="1"/>
											<feGaussianBlur stdDeviation="3"/>
											<feComposite in2="hardAlpha" operator="out"/>
											<feColorMatrix type="matrix" values="0 0 0 0 0.901961 0 0 0 0 0.611765 0 0 0 0 0.192157 0 0 0 0.27 0"/>
											<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_102_172"/>
											<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_102_172" result="shape"/>
											</filter>
											</defs>
											</svg>
											
									</li>
									
								</ul>                    
							</nav>
							<nav>
								<div class:navclass={navToggle} class="app-op">
									<table>

										<tbody>
											<tr>
												<td></td>
												<td></td>
												<td class="t-btn"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
													<path d="M6 6C6 3.78947 4.21053 2 2 2C1.45614 2 1 2.45614 1 3C1 3.54386 1.45614 4 2 4C3.22807 4 4 4.77193 4 6C4 6.54386 4.45614 7 5 7C5.54386 7 6 6.54386 6 6ZM17.4035 7C18.807 7 19.614 7.98246 19.3684 9.36842L18.4737 14.3684C18.2807 15.4211 17.5789 16 16.4912 16H8C6.77193 16 6 15.2281 6 14V7H17.4035ZM17.4035 5H4V14C4 16.2105 5.78947 18 8 18H16.4912C18.4211 18 20.0877 16.614 20.4386 14.7193L21.3333 9.7193C21.7719 7.26316 19.9123 5 17.4035 5ZM17 19C15.8947 19 15 19.8947 15 21C15 22.1053 15.8947 23 17 23C18.1053 23 19 22.1053 19 21C19 19.8947 18.1053 19 17 19ZM7 19C5.89474 19 5 19.8947 5 21C5 22.1053 5.89474 23 7 23C8.10526 23 9 22.1053 9 21C9 19.8947 8.10526 19 7 19Z" fill="var(--bl)"/>
												</svg>
													</td>
											</tr>
											<tr>
												<td></td>
												<td class="t-btn"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
													<path d="M3.89474 5.36851C2.78947 5.965 2 7.33342 2 8.56149V18.0001C2 20.2457 3.75439 22.0001 6 22.0001H18C20.2456 22.0001 22 20.2457 22 18.0001V8.56149C22 7.33342 21.2105 5.965 20.1053 5.36851L13.7719 1.8422C12.7544 1.28079 11.2456 1.28079 10.2281 1.8422L3.89474 5.36851ZM4.84211 7.1229L11.2105 3.59658C11.7018 3.31588 12.2982 3.31588 12.7895 3.59658L19.1579 7.1229C19.6842 7.4036 20 7.94746 20 8.56149V18.0001C20 19.2632 19.2632 20.0001 18 20.0001H6C4.73684 20.0001 4 19.2632 4 18.0001V8.56149C4 7.94746 4.31579 7.4036 4.84211 7.1229ZM22 9.31588C22 8.36851 21.0351 7.82465 20.2281 8.29834L12.7895 12.4211C12.2982 12.7018 11.7018 12.7018 11.2105 12.4211L3.77193 8.29834C2.96491 7.82465 2 8.36851 2 9.31588V18.0001C2 20.2457 3.75439 22.0001 6 22.0001H18C20.2456 22.0001 22 20.2457 22 18.0001V9.31588ZM20 9.31588V18.0001C20 19.2632 19.2632 20.0001 18 20.0001H6C4.73684 20.0001 4 19.2632 4 18.0001V9.31588C4 9.50886 3.84211 9.8422 3.42105 10.3861L10.2281 14.1755C11.2456 14.7369 12.7544 14.7369 13.7719 14.1755L20.5789 10.3861C20.1579 9.8422 20 9.50886 20 9.31588Z" fill="var(--bl)"/>
													</svg>
													</td>
												<td></td>
											</tr>
											<tr>
												<td class="t-btn"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
													<path d="M12.4561 4C13.0877 4 13.228 4.10526 13.2982 4.4386L13.3859 4.84211C13.5438 5.59649 14.0175 6.26316 14.8245 6.70176C14.9649 6.77193 15.035 6.82456 15.1227 6.87719C15.9122 7.38597 16.7368 7.45614 17.4561 7.24561L17.6315 7.17544C18.1754 7 18.421 7.08772 18.6842 7.57895L19.1754 8.40351C19.4736 8.92983 19.4561 9.10526 19.1754 9.35088L18.842 9.68421C18.3157 10.1754 17.9824 10.8772 17.9999 11.7719C17.9999 11.9123 17.9999 12.0702 17.9999 12.2105C17.9649 13.0175 18.2456 13.7719 18.842 14.3333L18.9999 14.4737C19.421 14.8596 19.4561 15.0877 19.1578 15.5965L18.7017 16.4211C18.4034 16.9298 18.2456 17 17.8596 16.8772L17.4385 16.7544C16.7368 16.5439 15.9298 16.614 15.1403 17.1228C15.0701 17.1754 14.9999 17.2105 14.8245 17.2982C14.0175 17.7368 13.5613 18.386 13.3859 19.1228L13.3508 19.3158C13.2456 19.8596 13.0526 20 12.4561 20H11.5438C10.9298 20 10.7894 19.8947 10.7192 19.5263L10.5964 19.0877C10.4385 18.4035 9.96485 17.7368 9.15783 17.2807C9.03503 17.2281 8.96485 17.1754 8.8245 17.1053C8.07011 16.614 7.24555 16.5439 6.5438 16.7544L6.36836 16.8246C5.8245 17 5.57889 16.9123 5.31573 16.4211L4.8245 15.5965C4.52625 15.0702 4.5438 14.8947 4.8245 14.6491L5.15783 14.3158C5.68415 13.8246 6.01748 13.1228 5.99994 12.2281C5.99994 12.0877 5.99994 11.9298 5.99994 11.7895C6.03503 10.9825 5.75433 10.2281 5.15783 9.66667L4.99994 9.52632C4.57889 9.14035 4.5438 8.91228 4.84204 8.40351L5.29819 7.57895C5.61397 7.07018 5.77187 6.98246 6.12275 7.08772L6.52625 7.22807C7.24555 7.45614 8.08766 7.38597 8.87713 6.87719C8.92976 6.84211 9.03503 6.78947 9.19292 6.70176C9.9824 6.26316 10.4561 5.59649 10.614 4.85965L10.6491 4.68421C10.7543 4.14035 10.9473 4 11.5438 4H12.4561ZM12.4561 2H11.5438C10.1578 2 8.9824 2.89474 8.68415 4.29825L8.64906 4.47368C8.59643 4.70175 8.5438 4.77193 8.21047 4.94737C8.1052 5.01754 7.91222 5.12281 7.77187 5.21053C7.49117 5.38596 7.40345 5.40351 7.14029 5.33333L6.73678 5.19298C5.61397 4.84211 4.31573 5.31579 3.57889 6.59649L3.08766 7.42105C2.40345 8.63158 2.63152 10.0526 3.64906 11L3.78941 11.1404C4.01748 11.3509 4.01748 11.386 3.99994 11.7193C3.99994 11.8947 3.99994 12.0877 3.99994 12.2632C4.01748 12.614 3.99994 12.6667 3.78941 12.8772L3.45608 13.1754C2.61397 13.9649 2.36836 15.3158 3.1052 16.5789L3.56134 17.4035C4.2631 18.6316 5.64906 19.1404 6.96485 18.7193L7.14029 18.6842C7.40345 18.5965 7.47362 18.614 7.77187 18.7895C7.91222 18.8947 8.07012 18.9825 8.22801 19.0526C8.5438 19.2281 8.59643 19.2982 8.66661 19.5789L8.75433 19.9825C9.01748 21.0877 10.0526 22 11.5438 22H12.4561C13.842 22 15.0175 21.1053 15.3157 19.7018L15.3508 19.5439C15.4034 19.2807 15.4561 19.2281 15.7719 19.0526C15.9122 18.9825 16.1052 18.8772 16.2456 18.7895C16.5438 18.614 16.614 18.5965 16.8771 18.6842L17.2982 18.807C18.3859 19.1404 19.6842 18.6842 20.421 17.4035L20.9122 16.5789C21.5964 15.3684 21.3684 13.9474 20.3508 13L20.2105 12.8596C19.9824 12.6491 19.9824 12.614 19.9999 12.2807C19.9999 12.1053 19.9999 11.9123 19.9999 11.7368C19.9824 11.386 19.9999 11.3333 20.2105 11.1228L20.5438 10.8246C21.3859 10.0351 21.6315 8.68421 20.8947 7.42105L20.4385 6.59649C19.7368 5.36842 18.3508 4.85965 17.035 5.2807L16.8596 5.31579C16.614 5.40351 16.5263 5.38596 16.228 5.21053C16.0701 5.10526 15.9122 5.01754 15.807 4.94737C15.4561 4.75439 15.4034 4.7193 15.3508 4.45614L15.2631 4.01754C15.0175 2.89474 13.9473 2 12.4561 2ZM7.99994 12C7.99994 14.2105 9.78941 16 11.9999 16C14.2105 16 15.9999 14.2105 15.9999 12C15.9999 9.78947 14.2105 8 11.9999 8C9.78941 8 7.99994 9.78947 7.99994 12ZM9.99994 12C9.99994 10.7719 10.7719 10 11.9999 10C13.228 10 13.9999 10.7719 13.9999 12C13.9999 13.2281 13.228 14 11.9999 14C10.7719 14 9.99994 13.2281 9.99994 12Z" fill="var(--bl)"/>
													</svg>
												</td>
												<td></td>
												<td></td>
											</tr>
											<tr>
												<td></td>
												<td></td>
												<td on:click={()=>{navToggle = !navToggle}} class="tc-btn"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
													<path d="M4.29825 5.70175L18.2982 19.7018C18.4737 19.8947 18.7193 20 19 20C19.5439 20 20 19.5439 20 19C20 18.7193 19.8947 18.4737 19.7018 18.2982L5.70175 4.29824C5.52632 4.10526 5.2807 4 5 4C4.45614 4 4 4.45614 4 5C4 5.2807 4.10526 5.52632 4.29825 5.70175ZM18.2982 4.29824L4.29825 18.2982C4.10526 18.4737 4 18.7193 4 19C4 19.5439 4.45614 20 5 20C5.2807 20 5.52632 19.8947 5.70175 19.7018L19.7018 5.70175C19.8947 5.52632 20 5.2807 20 5C20 4.45614 19.5439 4 19 4C18.7193 4 18.4737 4.10526 18.2982 4.29824Z" fill="var(--we)"/>
													</svg>
													</td>
											</tr>

										</tbody>
									</table>
								</div>
								<div on:click={nav} class="app-bt">
									<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
										<path d="M3 12C3 13.1053 3.89474 14 5 14C6.10526 14 7 13.1053 7 12C7 10.8947 6.10526 10 5 10C3.89474 10 3 10.8947 3 12ZM10 12C10 13.1053 10.8947 14 12 14C13.1053 14 14 13.1053 14 12C14 10.8947 13.1053 10 12 10C10.8947 10 10 10.8947 10 12ZM17 12C17 13.1053 17.8947 14 19 14C20.1053 14 21 13.1053 21 12C21 10.8947 20.1053 10 19 10C17.8947 10 17 10.8947 17 12ZM3 5C3 6.10526 3.89474 7 5 7C6.10526 7 7 6.10526 7 5C7 3.89474 6.10526 3 5 3C3.89474 3 3 3.89474 3 5ZM10 5C10 6.10526 10.8947 7 12 7C13.1053 7 14 6.10526 14 5C14 3.89474 13.1053 3 12 3C10.8947 3 10 3.89474 10 5ZM17 5C17 6.10526 17.8947 7 19 7C20.1053 7 21 6.10526 21 5C21 3.89474 20.1053 3 19 3C17.8947 3 17 3.89474 17 5ZM3 19C3 20.1053 3.89474 21 5 21C6.10526 21 7 20.1053 7 19C7 17.8947 6.10526 17 5 17C3.89474 17 3 17.8947 3 19ZM10 19C10 20.1053 10.8947 21 12 21C13.1053 21 14 20.1053 14 19C14 17.8947 13.1053 17 12 17C10.8947 17 10 17.8947 10 19ZM17 19C17 20.1053 17.8947 21 19 21C20.1053 21 21 20.1053 21 19C21 17.8947 20.1053 17 19 17C17.8947 17 17 17.8947 17 19Z" fill="#0C99FF"/>
										</svg>
								</div>
													   
							</nav>
						</div>
					</div>
				</div>
			</section>
		</main>
	</div>
</div>
<svelte:head>
	<title>maka house</title>
	<script>
		window.addEventListener("load", ()=>{
			document.querySelector(".preload-sect").classList.add("remove")
		})
	</script>
</svelte:head>

<style lang="scss">
	@import "./_config.scss";
	.navclass{
		clip-path: circle(1500px) !important;
		pointer-events: all !important;
		transition: 1s ease linear;
	}

	#layout{

		.lay{
			
			main{
				.section-one{
					z-index: 10;
					position: relative;
				}
			}
		}

	}
	
  
    #main-layout{
        .mn-layout{

            .navigation-top{
                padding:10px;
                position: fixed;
                top:0;
                left:0;
                width: 100%;
                z-index: 50;
                .nv-top{
                    padding:10px 0;
                    nav{
                        display: flex;
                        justify-content: space-between;
                        align-items: center;
                       
                        .about{
							background: var(--bg-we);
							padding: 8px;
							border-radius: 5px;
							box-shadow: rgba(0, 0, 0, 0.2) 3px 3px 3px 0;
							
							
							span{
								margin:0 3px;
								padding: 3px;
							}
                            
                        }
                    }
                }

            }
            .navigation-bottom{
                position: fixed;
                width: 100%;
                bottom: 0;
                left:0;
				padding: 4px;
				padding-top:0;
                .nv-bottom{
					display: flex;
					align-items: center;
					justify-content: space-between;
					nav:nth-child(2){
						padding:5px;
						
						display: flex;
						justify-content: center;
						align-items: center;
						.app-bt{
							padding: 10px; 
							border-radius: 4rem;
							background: var(--f-bl);
							

						}
					
						.app-op{
							position: fixed;
							right: 0;
							bottom:0;
							background: var(--f-bl);
							border-radius: 14px;
							clip-path: circle(0) ;
							transition: 1s ease linear;
							pointer-events: none;
							
							table{
								border-spacing: 20px ;
								tr{
									td{
										padding: 13.5px;
									}
									.t-btn{
										background: var(--we);
										border-radius: 8px;
										box-shadow: rgba(0, 0, 0, 0.22)0 0 7px 1px;
										svg{
											width: 20px;
										}
									}
									.tc-btn{
										background: rgba(255, 0, 0, 0.235);
										border-radius: 11px;
									}
									
								}
							}
							

						}
					}
                    nav:nth-child(1){
						flex: 1;
						border: var(--gd) solid 1px;
						border-radius: 7px;
						padding: 3px;
                    
                        ul{
                            display: flex;
                            justify-content: space-between;
							align-items: center;
                            padding:0;
                            margin:0;
                            list-style: none;
                            li{
                                @include font(var(--dbc), 0.7rem,500);
                                a{
                                    padding: 10px 15px;
                                }
                            }
                        }
                    }
                }
            }
        }
    }
    .about-content{
        background: var(--nv);
        position: fixed;
        width: 100%;
        top:0;
        left:0;
        height: 100vh;
        z-index: 100;
        clip-path: circle(0);
		pointer-events: none;
    

    }
</style>