<script>
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	import Sidebar from "./Sidebar.svelte";

	document.addEventListener("DOMContentLoaded", () => {
		const headerImage = document.querySelector(".header-image");

		window.addEventListener("scroll", () => {
			const scrollPosition =
				window.scrollY || document.documentElement.scrollTop;

			if (scrollPosition > 30) {
				headerImage.style.transform = "translateX(-100%)";
				headerImage.style.opacity = "0";
			} else {
				headerImage.style.transform = "translateX(0)";
				headerImage.style.opacity = "1";
			}
		});
	});
</script>

<Header />
<Sidebar />
<main>
	<div class="header-container">
		<h1 class="left-aligned-header">Software engineer</h1>
		<img src="pic2.png" alt="Description" class="header-image" />
	</div>

	<div class="centered-content">
		<p class="content-text">
			Hi, my name is Dudko Mikhail, I am software developer. Primary code
			in c++, but had experience in languages like: Rust, Python,
			C#(.NET).
		</p>
	</div>

	<h1 class="left-aligned-header">Skills</h1>
	<div class="centered-content">
		<ul class="content-list">
			<li>
				Strong knowledge of: C++17, STL, Git, Qt, Cmake, SQL, Linux,
				English
			</li>
			<li>
				Had experience with: gRPC, Rust, Python, boost, gtest, LLVM,
				docker
			</li>
		</ul>
	</div>

	<h1 class="left-aligned-header">Work Experience</h1>

	<h2 class="gradient-colored left-aligned-header">
		Baspro project / C++ programmer. <b class="gray"
			>(october 2020 - PRESENT, Tyumen, Russia)</b
		>
	</h2>

	<div class="centered-content">
		<ul class="content-list">
			<li>Desktop C++ applications development</li>
			<li>Applications for GNU/Linux and MS Windows operating systems</li>
			<li>
				Made solutions which involved multithreading and asynchronous
				programming
			</li>
			<li>GUI development using Qt framework</li>
			<li>Worked on ORM improvements and functionality</li>
			<li>Worked with Postgre, Sqlite, Oracle databases.</li>
			<li>
				Made an automated system for deploying applications using bash,
				python and powershell.
			</li>
			<li>Worked on distributed applications using gRPC communication</li>
			<li>Used to write unit tests using gtest library</li>
			<li>
				Developed a complex licensing system for company products in
				rust using tokio framework.
			</li>
			<li>
				Used different profiling tools like valgrind, gdb, VLD, VS
				profiler
			</li>
		</ul>
	</div>

	<h1 class="left-aligned-header">Education</h1>

	<h2 class="gradient-colored left-aligned-header">
		Tyumen State University
	</h2>
	<div class="centered-content">
		<p class="content-text">
			Bachelor of science in Cybersecurity september 2019 - august 2023,
			Tyumen, Russia Cybersecurity in networking and WEB and desktop
			applications
		</p>
	</div>

	<h2 class="gradient-colored left-aligned-header">
		Incheon National University
	</h2>

	<div class="centered-content">
		<p class="content-text">
			Computer science & engineering february 2022 - june 2022, Incheon,
			South Korea.<br />
			Took classes in machine learning and c++ applications development
		</p>
	</div>
</main>
<Footer />

<style>
	main {
		text-align: center;
		padding: 0;
		margin: 0 auto;
		margin-top: 200px;
	}

	.content-list {
		text-align: left;
	}

	.header-container {
		position: relative;
	}

	.left-aligned-header {
		z-index: 2;
		position: relative;
	}

	.gray {
		color: rgb(101, 101, 101);
	}

	.header-image {
		position: absolute;
		top: -85px;
		left: 0;
		width: 280px;
		height: auto;
		z-index: 3;
		transition:
			transform 0.5s ease-out,
			opacity 0.5s ease-out;
		will-change: transform, opacity;
	}

	.hide-image {
		transform: translateX(-100%);
		opacity: 0;
	}

	.left-aligned-header {
		text-align: left;
		margin-left: 0;
		margin-top: 100px;
		margin-right: auto;
		background-image: linear-gradient(to right, gray, white);
		color: #1b1b1b;
		padding: 10px;
		width: 50%;
		padding-left: 210px;
	}

	.gradient-colored {
		background-image: none;
	}

	.gradient-colored::before {
		content: "";
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: linear-gradient(to right, black 10%, white 50%);
		border-radius: inherit;
		box-sizing: border-box;
		-webkit-mask:
			linear-gradient(to left, transparent, black 99%) top / 100% 2px
				no-repeat,
			linear-gradient(to left, transparent, black 99%) bottom / 100% 2px
				no-repeat;
		mask:
			linear-gradient(to left, transparent, black 99%) top / 100% 2px
				no-repeat,
			linear-gradient(to left, transparent, black 99%) bottom / 100% 2px
				no-repeat;
	}

	.centered-content {
		color: #000000;
		margin-left: 20%;
		margin-right: 20%;
		font-size: 2em;
	}

	.content-text {
		margin-top: 50px;
		text-align: justify;
		text-justify: inter-word;
	}

	h1 {
		color: #000000;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (max-width: 810px) {
		h1 {
			font-size: 2em;
		}

		h2 {
			font-size: 0.8em;
		}

		.centered-content {
			margin-left: 10%;
			margin-right: 10%;
			font-size: 1.6em;
		}

		.header-image {
			top: -60px;
			width: 200px;
		}

		.left-aligned-header {
			padding-left: 22%;
			margin-top: 50px;
		}
	}

	@media (max-width: 400px) {
        h1 {
			font-size: 1.3em;
		}

		.header-image {
			top: -42px;
			width: 140px;
		}

		.centered-content {
			font-size: 1.2em;
		}

		.left-aligned-header {
			padding-left: 12%;
		}

		.gradient-colored::before {
			background: linear-gradient(to right, black , white );
		}
    }
	
</style>
