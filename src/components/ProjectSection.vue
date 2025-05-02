<script setup>
import { ref, computed } from 'vue';
const Projects = ref([
    {
        id: 1,
        category: 'prototypes',
        image: new URL('@/assets/project-imgs/lithaven-thumbnail.png', import.meta.url).href,
        title: 'Lithaven',
        description: 'Lithaven is an app designed to support readers, of all ages, in their journey to find and read new books.',
        technologies: ['Figma'],
        gitURL: '',
        webURL: 'https://www.figma.com/proto/D6aUsCMECvoVPeFI1Zsoze/Lithaven?node-id=278-4195&starting-point-node-id=278%3A4195&t=mNqF32r3RrS1znBD-1'
    },
    {
        id: 2,
        category: 'websites',
        image: new URL('@/assets/project-imgs/climacast-thumbnail.png', import.meta.url).href,
        title: 'Climacast',
        description: 'An intuitive weather application designed to provide users with real-time forecasts and dynamic weather visualizations.',
        technologies: ['HTML', 'CSS', 'JavaScript', 'Vue.js'],
        gitURL: 'https://github.com/lachlanallen/climacast/tree/gh-pages',
        webURL: 'https://lachlanallen.github.io/climacast/'
    },
    {
        id: 3,
        category: 'websites',
        image: new URL('@/assets/project-imgs/sprout-grow-thumbnail.png', import.meta.url).href,
        title: 'Sprout & Grow',
        description: 'A dynamic website for Sprout & Grow, a fictional client passionate about sustainable gardening.',
        technologies: ['HTML', 'CSS'],
        gitURL: '',
        webURL: 'https://wcet.waketech.edu/ltallen3/WEB140/Sprout_Grow_Website/'
    },
    {
        id: 4,
        category: 'websites',
        image: new URL('@/assets/project-imgs/pokesearch-thumbnail.png', import.meta.url).href,
        title: 'PokeSearch',
        description: 'A web app that utilizes PokeAPI to display Generation 7 Pokemon and their information.',
        technologies: ['HTML', 'Tailwind CSS', 'JavaScript', 'React.js'],
        gitURL: 'https://github.com/lachlanallen/PokeSearch',
        webURL: 'https://lachlanallen.github.io/PokeSearch/'
    },
    {
        id: 5,
        category: 'prototypes',
        image: new URL('@/assets/project-imgs/alpine-thumbnail.png', import.meta.url).href,
        title: 'Alpine Serenity Inn',
        description: 'A bed and breakfast prototype designed to offer users a seamless experience in booking their stay.',
        technologies: ['Figma'],
        gitURL: '',
        webURL: 'https://www.figma.com/proto/Z8SkfiiFyPHjwNZr62Qnp8/Alpine-Serenity-Inn?node-id=189-3451&t=HiESICVIautMuYmk-1&scaling=min-zoom&content-scaling=fixed&page-id=189%3A3450&starting-point-node-id=189%3A3580'
    },
]);

const selectedCategory = ref('all');
const filteredProjects = computed(() => {
    if (selectedCategory.value === 'all') {
        return Projects.value;
    }
    return Projects.value.filter(project => project.category.toLocaleLowerCase() === selectedCategory.value.toLocaleLowerCase());
});

</script>

<template>
    <main id="projects" class="project-preview-container text-primary mt-16 px-4 xl:pl-16">
        <h2 class="text-4xl font-bold font-serif text-primary text-left mb-8">My 
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">Projects</span>
                </h2>
        <!-- Category Filter Buttons -->
        <div class="flex space-x-4 mb-4 mt-5 md:mt-3">
            <button 
                class="capitalize font-medium border-2 py-2 px-5 rounded-3xl transition-colors duration-300"
                :class="[
                    selectedCategory === category 
                        ? 'bg-tertiary text-light border-tertiary'
                        : 'bg-secondary text-tertiary border-secondary hover:bg-tertiary hover:border-tertiary hover:text-light'
                ]"
                v-for="category in ['all', 'websites', 'prototypes']" 
                :key="category"
                @click="() => selectedCategory = category"
            >
                {{ category }}
            </button>
        </div>
        <!-- Project Grid -->
        <section
            class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
            data-aos="fade-right">
            <!-- Loop through filtered projects -->
            <section v-for="project in filteredProjects" :key="project.id"
                class="relative group border border-gray-300 rounded-2xl overflow-hidden">
                <img class="img-preview w-full h-60 object-cover" :src="project.image"
                    :alt="project.title + ' preview'" />
                <!-- Overlay with project details -->
                <div class="overlay absolute inset-0 bg-primary bg-opacity-0 group-hover:bg-opacity-80 transition-all duration-500 flex flex-col items-center justify-center text-white p-4 opacity-0 group-hover:opacity-100">
                    <h3 class="text-xl font-bold mb-2">{{ project.title }}</h3>
                    <p class="text-center text-sm mb-3">{{ project.description }}</p>
                    <div class="flex space-x-2">
                        <a v-if="project.gitURL" :href="project.gitURL" target="_blank" class="border-2 py-2 px-5 rounded-3xl hover:text-secondary">GitHub</a>
                        <a v-if="project.webURL" :href="project.webURL" target="_blank" class="border-2 py-2 px-5 rounded-3xl hover:text-secondary">
                            {{ project.category === 'prototypes' ? 'View Prototype' : 'View Website' }}
                        </a>
                    </div>
                </div>
            </section>
        </section>
        <div class="flex justify-center mt-6 md:mt-0">
            <router-link to="/projects" class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                <span
                    class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                <span class="relative flex items-center justify-center text-dark font-medium">View All Projects</span>
            </router-link>
        </div>
    </main>
</template>