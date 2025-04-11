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
        year: "2018 - 2020"
    }
])
</script>

<template>
    <section class="text-primary mt-18" id="about">
        <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
            <div class="h-24 w-64 bg-gradient-to-br from-accent to-secondary-accent blur-2xl opacity-20"></div>
        </div>
        <!-- Education Section -->
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl font-bold font-serif text-primary text-left mb-8">My Education</h2>
                <div class="space-y-8 py-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center p-4 md:w-[90%] w-full rounded-xl bg-tertiary shadow-lg border border-primary"
                    >
                        <div class="pl-4">
                            <img src="@/assets/book.svg" alt="Education" />
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-secondary to-light lg:text-xl">
                                {{ element.degree }}
                            </h3>
                            <p class="text-light">{{ element.concentration }}</p>
                            <p class="text-light">{{ element.institution }}</p>
                            <p class="text-light italic">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- About Section -->
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="text-4xl font-bold font-serif text-primary md:text-center text-left mb-4">More 
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">About Me</span>
                </h2>
                <p class="text-base lg:text-lg mt-8 py-8">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro, nihil dignissimos. Eius accusantium architecto doloremque deleniti possimus necessitatibus, alias quam modi qui perferendis sequi vero illum doloribus quos tenetur nisi. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aspernatur, optio porro. Voluptas corporis soluta delectus mollitia aliquid dolor enim illo repellat dolores quas numquam eaque, necessitatibus quaerat, error deleniti laboriosam.
                </p>
                <div class="grid grid-cols-3 gap-4 max-w-lg pt-8">
                    <div class="text-center rounded-xl bg-accent shadow-lg border border-accent-dark p-3">
                        <h4 class="text-dark font-bold font-serif text-xl sm:text-2xl lg:text-3xl">Lorem</h4>
                        <p class="text-sm sm:text-base text-dark">Ipsum</p>
                    </div>
                    <div class="text-center rounded-xl bg-accent shadow-lg border border-accent-dark p-3">
                        <h3 class="text-dark font-bold font-serif text-xl sm:text-2xl lg:text-3xl">Lorem</h3>
                        <p class="text-sm sm:text-base text-dark">Ipsum</p>
                    </div>
                    <div class="text-center rounded-xl bg-accent shadow-lg border border-accent-dark p-3">
                        <h3 class="text-dark font-bold font-serif text-xl sm:text-2xl lg:text-3xl">Lorem</h3>
                        <p class="text-sm sm:text-base text-dark">Ipsum</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>