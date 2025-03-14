<template>
  <div id="projects-view">
      <h1>:Projects</h1>

      <div id="experience">
          <ul id="experiences">
              <li v-for="project in projects" :key="project.title" class="experience-item">
                  <div class="experience-header">
                      <div>
                          <div class="job-title">{{ project.title }}</div>
                          <!-- <div class="company-location">{{ project.company }}, {{ job.location }}</div> -->
                      </div>
                      <!-- <div class="date-range">{{ job.dateRange }}</div> -->
                  </div>
                  <ul class="responsibilities">
                      <li v-for="note in project.notes" :key="note">
                          {{ note }}
                      </li>
                  </ul>
              </li>
          </ul>
      </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const projects = ref(
	[
		{
			title: 'Cancer Detector',
			languages: ['Python'],
			frameworks: ['Pytorch'],
			notes: [
				'Built a Deep Neural Network that identifies cancerous cells in medical scans.',
				'Used a Deep Convolution Network, PyTorch and a Kaggle dataset to train the model.'
			]
		},
		{
			title: 'Pokemon',
			languages: ['C++'],
			frameworks: ['GCC', 'Makefile'],
			notes: [
				'Created Pokemon and simulated battles with their types, strength & weaknesses',
				'Used C++, GCC and MAKEFILE'
			]
		},
		{
			title: 'Olympsis',
			languages: ['Swift', 'Golang', 'Typescript'],
			frameworks: ['SwiftUI', 'NuxtJS'],
			notes: [
				'Built a platform where athletes can meet together and plan sport activities.',
				'Used Golang & MongoDB to build REST API. Used SwiftUI for the mobile client.'
			]
		}
	]
)
</script>

<style scoped>
#projects-view {
  width: 100%;
  display: flex;
  margin: 0 auto;
  max-width: 80rem;
  overflow-y: scroll;
  flex-direction: column;
  height: calc(100dvh - 50px);

  h1 {
      margin: 2rem;
  }

  h2 {
      margin-bottom: 1rem;
  }

  #experience {
      margin: 0rem 4rem;
  }

  .experience-item {
      margin-left: 1rem;
      position: relative;
      margin-bottom: 30px;
  }

  .experience-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 10px;
  }

  .job-title {
      font-size: 16px;
      font-weight: bold;
      text-transform: uppercase;
  }

  .company-location {
      
  }

  .date-range {
      
      font-size: 14px;
  }

  .responsibilities {
      list-style-type: none;
      padding-left: 20px;
      margin-top: 10px;
  }

  .responsibilities li {
      position: relative;
      margin-bottom: 8px;
      line-height: 1.4;
      
  }

  .responsibilities li:not(:last-child)::before {
      top: 30px;
      width: 2px;
      left: -20px;
      bottom: -10px;
      position: absolute;
      
  }
}

@media (max-width: 1000px) {
#resume-view {

  h1 {
      margin: 1.5rem;
  }

  h2 {
      color: black;
      margin-bottom: 1rem;
  }

  #experience {
      margin: 0rem 4rem;
  }
}
}
</style>