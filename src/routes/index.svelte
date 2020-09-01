<style>
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	figure {
		margin: 0 0 1em 0;
	}

	img {
		width: 100%;
		max-width: 960px;
		margin: 0 0 1em 0;
	}

	p {
		margin: 1em auto;
	}

	.logo-btn {
		background-color: cornflowerblue;
		padding: 0.5em;
		color: white;
		width: 30%;
		text-align: center;
		margin: auto;
		font-size: 1.6rem;
	}

	@media (max-width: 800px) {
		.logo-btn {
			width: 80%;
		}
	}
</style>

<svelte:head>
	<title>지상 최대의 영어 작전</title>
	<meta name="description" content="팟캐스트 지상 최대의 영어 작전 홈페이지" />
	<meta name="keywords" content="영어 학습 팟캐스트"/>
	<!-- Global site tag (gtag.js) - Google Analytics -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=UA-45888586-1"></script>
	<script>
	  window.dataLayer = window.dataLayer || [];
	  function gtag(){dataLayer.push(arguments);}
	  gtag('js', new Date());

	  gtag('config', 'UA-45888586-1');
	</script>
</svelte:head>

<figure>
	<a href="http://www.podbbang.com/ch/11200">
		<img alt='Podcast screenshot' src='podcast-logo.jpg'>
	</a>
	<figcaption>'지상 최대의 영어 작전'은 '봄나무가 꾸는 꿈'의 대표 팟캐스트입니다.</figcaption>
</figure>

<div class="logo-btn">
	<a href="http://www.podbbang.com/ch/11200">
		팟캐스트 바로 가기
	</a>
</div>
