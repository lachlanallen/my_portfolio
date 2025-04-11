<script setup>
import { ref } from 'vue';
const Skills = ref([
    {
        id: 1,
        name: "HTML5 & CSS3",
        width: "95%"
    },
    {
        id: 2,
        name: "JavaScript",
        width: "85%"
    },
    {
        id: 3,
        name: "Vue.js",
        width: "85%"
    },
    {
        id: 4,
        name: "React.js",
        width: "70%"
    },
    {
        id: 5,
        name: "Ux/UI Design",
        width: "95%"
    },
    {
        id: 6,
        name: "Figma",
        width: "95%"
    }
]);

const Experience = ref([
    {
        id: 1,
        title: "Instructional Assistant",
        company: "University of North Carolina at Charlotte",
        duration: "May 2023 - May 2024",
        description: "Lorem impsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum."
    },
    {
        id: 2,
        title: "Barista",
        company: "Barnes & Noble, Inc.",
        duration: "August 2024 - Present",
        description: "Lorem impsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum."
    },
]);

</script>

<template>
    <section class="text-primary mt-18" id="skills">
        <!-- Background Gradients -->
        <div class="absolute right-0 top-[110rem] h-full w-full justify-end">
            <span class="flex opacity-20">
                <span class="w-25 h-50 rounded-l-full flex bg-accent blur-2xl"></span>
                <span class="w-25 h-50 rounded-r-full flex bg-secondary-accent blur-2xl"></span>
            </span>
        </div>
        <!-- Skills Section -->
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
                <h2 class="text-4xl font-bold font-serif text-primary text-left mb-4">My
                    <span
                        class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">Skills</span>
                </h2>
                <div class="mt-8" v-for="skill in Skills" :key="skill.id">
                    <div class="flex items-end justify-between" data-aos="fade-right">
                        <h4 class="font-semibold uppercase text-primary">{{ skill.name }}</h4>
                        <h3 class="text-2xl font-bold text-primary">{{ skill.width }}</h3>
                    </div>
                    <!-- Skill Progress Bar -->
                    <div class="mt-2 h-1 w-fu;; bg-accent rounded-full">
                        <div class="h-1 bg-accent-darker rounded-full" :style="`width :${skill.width}`"></div>
                    </div>
                </div>
            </div>
            <!-- Experience Section -->
            <div data-aos="flip-left">
                <h2 class="text-4xl font-bold font-serif text-primary text-left mb-8 md:text-center md:mt-0 mt-8">My
                    Experience</h2>
                <div class="space-y-8 py-8 flex flex-col items-center" data-aos="fade-left">
                    <div v-for="element in Experience" :key="element.id"
                        class="flex items-center p-4 md:w-[90%] w-full rounded-xl bg-tertiary shadow-lg border border-primary">
                        <div class="pl-4">
                            <img src="@/assets/briefcase.svg" alt="Briefcase" />
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3
                                class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-secondary to-light">
                                {{ element.title }}</h3>
                            <p class="text-light">{{ element.company }}</p>
                            <p class="text-light italic">{{ element.duration }}</p>
                            <p class="text-light">{{ element.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>