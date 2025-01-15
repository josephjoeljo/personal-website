<template>
	<div id="home-view">

		<!-- Profile -->
		<div id="profile">
			<img src="../assets/profile.jpeg" class="profile"/>

			<div id="links">
				<div class="link">
					<Label text="X" color="#19A026"/>
					<a class="label" href="https://x.com/josephjoeljo">@josephjoeljo</a>
				</div>

				<div class="link">
					<Label text="in" color="#5073DC"/>
					<a class="label" href="https://www.linkedin.com/in/joel-j-52261a101/">joel-j-52261a101</a>
				</div>

				<div class="link">
					<Label text="Github" color="#E63939"/>
					<a class="label" href="https://github.com/josephjoeljo">josephjoeljo</a>
				</div>

				<div class="link">
					<Label text="Email" color="#D0C119"/>
					<div class="label" @click="navigateToMail">joeljordanjoseph@gmail.com</div>
				</div>
			</div>
		</div>

		<!-- About Me -->
		<div id="about">
			<h1>:About Me</h1>
			<p>
				I was born in Haiti with an insatiable curiosity about how things work. This natural inclination often led me to disassemble gadgets and toys around the house—a habit that both frustrated and intrigued my parents.
				<br>
				<br>
				I earned a Bachelor of Science in Computer Science from Brigham Young University, where I worked on a variety of projects and contributed to computer vision research. While I love all areas of computer science, I am especially passionate about data-driven projects, machine learning, and systems engineering.
				<br>
				<br>
				Outside of my professional interests, I am polyglot and a car enthusiast who enjoys working on vehicles in my free time. These pursuits reflect my lifelong love for learning, problem-solving, and creating—values that guide both my personal and professional journey.
			</p>
		</div>
	</div>
</template>

<script setup lang="ts">
import Label from '@/components/Label.vue'

function navigateToMail() {
	document.location = 'mailto:joeljordanjoseph@gmail.com'
}

function downloadResume() {
	window.open('src/assets/Resume.pdf')
}
</script>

<style scoped>
#home-view {
	display: flex;
	overflow-y: scroll;
	background-color: white;
	height: calc(100vh - 50px);

	#profile {
		margin: 2rem;

		img {
			max-width: 20rem;
		}

		#links {
			.link {
				display: flex;
				margin: 0.5rem;

				.label {
					color: black;
					cursor: pointer;
					margin-left: 0.5rem;
					text-decoration: none;
				}
			}
		}
	}

	#about {
		margin: 3rem;

		h1 {
			color: black;
		}

		p {
			margin: 1rem 0rem 0rem 2rem;
			color: black;
		}
	}
}

@media (max-width: 1000px) {
	#home-view {
		flex-direction: column;

		#profile {
			margin: auto;
			margin-top: 2rem;
			width: fit-content;
		}

		#about {
			margin: 1.5rem;

			p {
				margin: 0.5rem 0rem 0rem 1rem;
			}
		}
	}
}
</style>
