<script setup>
import { ref } from 'vue';
const education = ref([
    {
        id: 1,
        degree: "Front-End Development Certificate",
        institution: "Wake Technical Community College",
        year: "2024 - 2025"
    },
    {
        id: 2,
        degree: "Bachelor of Art in Computer Science",
        institution: "University of North Carolina at Charlotte",
        concentration: "Concentrating in Human Computer Interaction",
        year: "2022 - 2024"
    },
    {
        id: 3,
        degree: "Associate of Science",
        institution: "Guilford Technical Community College",
        year: "2018 - 2022"
    }
]);

const Experience = ref([
    {
        id: 1,
        title: "Instructional Assistant",
        company: "University of North Carolina at Charlotte",
        duration: "May 2023 - May 2024",
        description: [
            "Provided individualized academic support, helping students overcome challenges.",
            "Fostered a respectful and inclusive classroom by mediating conflicts.",
            "Balanced rigorous coursework with grading and developing course assignments.",
            "Ensured clear communication with students and faculty, promptly addressing concerns.",
            "Held regular office hours to deepen student understanding of course material."
        ]
    },
    {
        id: 2,
        title: "Barista",
        company: "Barnes & Noble, Inc.",
        duration: "August 2024 - Present",
        description: [
            "Delivered excellent customer service through food and beverage preparation.",
            "Maintained a clean, organized workspace while managing inventory and safety compliance.",
            "Created a welcoming environment, assisting customers with menu choices and transactions."
        ]
    },
]);

</script>

<template>
    <section class="text-primary mt-18">
        
        <div class="md:grid md:grid-cols-2 gap-8 items-start py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <!-- Education Section -->
            <div data-aos="flip-left">
                <h2 class="text-4xl font-bold font-serif text-primary text-left mb-8 md:text-center md:mt-0 mt-8">My
                    <span
                        class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">Education</span>
                </h2>
                <div class="space-y-8 py-8 flex flex-col items-center" data-aos="fade-left">
                    <div v-for="element in education" :key="element.id"
                        class="flex items-start p-4 md:w-[90%] w-full rounded-xl bg-tertiary shadow-lg border border-primary">
                        <div class="pl-4 mt-1">
                            <img src="@/assets/book.svg" alt="Book" />
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3
                                class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-secondary to-light">
                                {{ element.degree }}</h3>
                            <p class="text-light">{{ element.concentration }}</p>
                            <p class="text-light italic">{{ element.institution }}</p>
                            <p class="text-light">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Experience Section -->
            <div data-aos="flip-left">
                <h2 class="text-4xl font-bold font-serif text-primary text-left mb-8 md:text-center md:mt-0 mt-8">My
                    <span
                        class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">Experience</span>
                </h2>
                <div class="space-y-8 py-8 flex flex-col items-center" data-aos="fade-left">
                    <div v-for="element in Experience" :key="element.id"
                        class="flex items-start p-4 md:w-[90%] w-full rounded-xl bg-tertiary shadow-lg border border-primary">
                        <div class="pl-4 mt-1">
                            <img src="@/assets/briefcase.svg" alt="Briefcase" />
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3
                                class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-secondary to-light">
                                {{ element.title }}</h3>
                            <p class="text-light">{{ element.company }}</p>
                            <p class="text-light italic">{{ element.duration }}</p>
                            <ul class="text-light list-disc pl-5">
                                <li v-for="(item, index) in element.description" :key="index">{{ item }}</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>