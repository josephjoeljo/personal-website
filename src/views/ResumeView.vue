<template>
    <div id="resume-view">
        <h1>:Resume</h1>

        <div id="experience">
            <h2>Experience</h2>
            <ul id="experiences">
                <li v-for="job in experiences" :key="job.title" class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">{{ job.title }}</div>
                            <div class="company-location">{{ job.company }}, {{ job.location }}</div>
                        </div>
                        <div class="date-range">{{ job.dateRange }}</div>
                    </div>
                    <ul class="responsibilities">
                        <li v-for="responsibility in job.responsibilities" :key="responsibility">
                            {{ responsibility }}
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const experiences = ref(
    [
        {
            title: 'AI Application Engineer',
            company: 'Passivelogic',
            location: 'Salt Lake City, UT',
            dateRange: '03/23-Present',
            responsibilities: [
                'Working on web applications to help create digital twins for micro climate simulation',
                'Working on applications fine tuning models with real world data to fit ideal eﬃciency curves.',
                'Built and maintained internal tools to automate database seeding of model data, streamlining development workflows.'
            ]
        },
        {
            title: 'Fullstack Engineer',
            company: 'Stutor',
            location: 'Lehi, UT',
            dateRange: '07/21-11/22',
            responsibilities: [
                'Created DevOps pipelines for automated testing and deployment of APIs, reducing deployment time by 40%',
                'Created detailed system architecture documentation to support onboarding and collaboration with external engineers',
                'Managed backend services using TypeScript and Node.js, hosted on Google Cloud Platform (GCP), ensuring high availability and fault tolerance.'
            ]
        },
        {
            title: 'Research Assistant',
            company: 'Brigham Young University',
            location: 'Provo, UT',
            dateRange: '05/22-08/22',
            responsibilities: [
                'Developed ensemble models for fine-grained classification of butterfly species, improving classification accuracy by 15%.',
                'Implemented object recognition and tracking with YOLOv5 and fine-tuned MobileNet for classification tasks',
                'Collaborated with researchers to share knowledge and deliver project milestones on time.'
            ]
        },
        {
            title: 'Technical Specialist',
            company: 'The Convenient Company',
            location: 'Draper, UT',
            dateRange: '12/18-01/21',
            responsibilities: [
                'Created automation scripts to streamline order processing, reducing manual effort by 30%.',
                'Maintained and updated the company website using VueJS and JavaScript, improving performance and user engagement.',
                'Repaired hundreds of Apple devices and other electronics, ensuring customer satisfaction and retention.'
            ]
        }
    ]
)
</script>

<style scoped>
#resume-view {
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