<script setup>
import lithavenImg from '@/assets/project-imgs/lithaven-thumbnail.png';
import sproutGrowImg from '@/assets/project-imgs/sprout-grow-thumbnail.png';
import pokesearchImg from '@/assets/project-imgs/pokesearch-thumbnail.png';
import alpineImg from '@/assets/project-imgs/alpine-thumbnail.png';
import climacastImg from '@/assets/project-imgs/climacast-thumbnail.png';
import { defineAsyncComponent } from 'vue';
import lithavenCaseStudy from '@/assets/case-studies/Allen-CaseStudy.pdf';
import alpineCaseStudy from '@/assets/case-studies/Allen-CaseStudy2.pdf';
const FooterSection = defineAsyncComponent(() => import('@/components/FooterSection.vue'));
</script>

<template>
    <main id="projects" class="project-container grid grid-cols-1 gap-8 p-8 md:px-40">
        <h2 class="text-4xl font-bold font-serif text-primary text-left">My
            <span
                class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">Projects</span>
        </h2>
        <!-- Project 1 -->
        <section class="project grid grid-cols-1 md:grid-cols-2 gap-4 text-tertiary">
            <img class="project-img w-full rounded-3xl md:pr-4" :src="lithavenImg" alt="Lithaven app preview" />
            <div class="lithaven project-info flex flex-col justify-evenly gap-4 md:col-start-2">
                <h1 class="text-2xl font-bold font-serif text-primary">Lithaven | UX Design Project</h1>
                <p>
                    Lithaven is an app designed to support readers, of all ages, in
                    their journey to find and read new books. Lithaven is a book
                    cataloging application where users can search, save, review, and
                    organize books they have read or are interested in reading. Users
                    will also be able to track their reading progress and set reading
                    goals for themselves. Lithaven aims to create a community where
                    users can find other like-minded readers and engage in book
                    discussions.
                </p>
                <h4 class="text-lg font-semibold">Key Achievements</h4>
                <ul class="w-4/5 ml-8 list-disc">
                    <li>
                        Conducted comprehensive user research to understand readers’ pain
                        points, preferences, and behaviors.
                    </li>
                    <li>
                        Utilized iterative design processes, refining concepts based on
                        user feedback loops.
                    </li>
                    <li>
                        Developed a high-fidelity Figma prototype, showcasing seamless
                        interactions and visual aesthetics.
                    </li>
                </ul>
                <div class="btn-container flex gap-4">
                    <a href="https://www.figma.com/proto/D6aUsCMECvoVPeFI1Zsoze/Lithaven?node-id=278-4195&starting-point-node-id=278%3A4195&t=mNqF32r3RrS1znBD-1"
                        target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View
                            Project</span>
                    </a>
                    <a :href="lithavenCaseStudy" target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View Case
                            Study</span>
                    </a>
                </div>
            </div>
        </section>
        <!-- Project 2 -->
        <section class="project grid grid-cols-1 md:grid-cols-2 gap-4 text-tertiary">
            <img class="project-img w-full rounded-3xl md:pl-4 md:col-start-2" :src="climacastImg"
                alt="Climacast website preview" />
            <div class="pokesearch project-info flex flex-col justify-evenly gap-4 md:col-start-1 md:row-start-1">
                <h1 class="text-2xl font-bold font-serif text-primary">Climacast | Vue.js Web App</h1>
                <p>
                    Climacast is an intuitive weather application designed to provide users with real-time forecasts and dynamic weather visualizations.
                </p>
                <h4 class="text-lg font-semibold">Key Achievements</h4>
                <ul class="w-4/5 ml-8 list-disc">
                    <li>
                        Designed an accessible and user-friendly interface, prioritizing intuitive navigation.
                    </li>
                    <li>
                        Integrated OpenWeather API to deliver accurate, up-to-date weather data.
                    </li>
                    <li>
                        Developed interactive charts using Chart.js to visualize temperature, precipitation, and other key metrics.
                    </li>
                </ul>
                <div class="btn-container flex gap-4">
                    <a href="https://lachlanallen.github.io/climacast/" target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View
                            Project</span>
                    </a>
                </div>
            </div>
        </section>
        <!-- Project 3 -->
        <section class="project grid grid-cols-1 md:grid-cols-2 gap-4 text-tertiary">
            <img class="project-img w-full rounded-3xl md:pr-4 " :src="sproutGrowImg"
                alt="Sprout and Grow website preview" />
            <div class="alt-info project-info flex flex-col justify-evenly gap-4 md:col-start-2">
                <h1 class="text-2xl font-bold font-serif text-primary">Sprout & Grow | Front-End Web Development Project
                </h1>
                <p>
                    Developed a dynamic, five-page website for Sprout & Grow, a
                    fictional client passionate about sustainable gardening. The site
                    includes a Home, About, Products, Events, and Event Registration
                    page.
                </p>
                <h4 class="text-lg font-semibold">Key Achievements</h4>
                <ul class="w-4/5 ml-8 list-disc">
                    <li>
                        Website Construction: Created the entire site from scratch,
                        adhering to semantic HTML standards.
                    </li>
                    <li>
                        Responsive Design: Ensured seamless adaptability across different
                        screen sizes.
                    </li>
                    <li>
                        User-Centered: Clear navigation, meaningful hyperlinks, and a
                        harmonious layout.
                    </li>
                </ul>
                <div class="btn-container flex gap-4">
                    <a href="https://wcet.waketech.edu/ltallen3/WEB140/Sprout_Grow_Website/" target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View
                            Project</span>
                    </a>
                </div>
            </div>
        </section>
        <!-- Project 4 -->
        <section class="project grid grid-cols-1 md:grid-cols-2 gap-4 text-tertiary">
            <img class="project-img w-full rounded-3xl md:pl-4 md:col-start-2" :src="pokesearchImg"
                alt="PokeSearch website preview" />
            <div class="pokesearch project-info flex flex-col justify-evenly gap-4 md:col-start-1 md:row-start-1">
                <h1 class="text-2xl font-bold font-serif text-primary">PokeSearch | React.js Web App</h1>
                <p>
                    Search for your favorite Pokémon with PokeSearch! This web app
                    utilizes PokeAPI to display Generation 7 pokemon and their
                    information.
                </p>
                <h4 class="text-lg font-semibold">Key Achievements</h4>
                <ul class="w-4/5 ml-8 list-disc">
                    <li>
                        Designed a responsive, interactive UI with an emphasis on user engagement and clarity of information architecture.

                    </li>
                    <li>
                        Created a component-based layout in React and Tailwind CSS to display real-time Pokémon data from the PokéAPI.

                    </li>
                    <li>
                        Users can explore detailed information about their favorite
                        Generation 7 Pokémon using a user-friendly interface with
                        responsive components.
                    </li>
                </ul>
                <div class="btn-container flex gap-4">
                    <a href="https://lachlanallen.github.io/PokeSearch/" target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View
                            Project</span>
                    </a>
                </div>
            </div>
        </section>
        <!-- Project 5 -->
        <section class="project grid grid-cols-1 md:grid-cols-2 gap-4 text-tertiary">
            <img class="project-img w-full rounded-3xl md:pr-4" :src="alpineImg"
                alt="Alpine Serenity Inn website preview" />
            <div class="alt-info project-info flex flex-col justify-evenly gap-4 md:col-start-2">
                <h1 class="text-2xl font-bold font-serif text-primary">Alpine Serenity Inn | UX Design Project</h1>
                <p>
                    Alpine Serenity Inn is a bed and breakfast prototype designed to offer users a seamless experience
                    in
                    booking their stay. The website features a variety of pages, including rooms, menus, and amenities.
                    Alpine Serenity Inn aims to provide an intuitive and user-friendly platform for guests to explore
                    the inn's offerings and easily make reservations.
                </p>
                <h4 class="text-lg font-semibold">Key Achievements</h4>
                <ul class="w-4/5 ml-8 list-disc">
                    <li>
                        Conducted user research to understand potential guests' preferences, needs, and booking
                        behaviors.
                    </li>
                    <li>
                        Employed iterative design processes, continuously refining concepts based on user feedback and
                        usability testing.
                    </li>
                    <li>
                        Developed a high-fidelity Figma prototype, showcasing a visually appealing and intuitive
                        interface that enhances the overall user experience.
                    </li>
                </ul>
                                <div class="btn-container flex gap-4">
                    <a href="https://www.figma.com/proto/Z8SkfiiFyPHjwNZr62Qnp8/Alpine-Serenity-Inn?node-id=189-3451&t=HiESICVIautMuYmk-1&scaling=min-zoom&content-scaling=fixed&page-id=189%3A3450&starting-point-node-id=189%3A3580" target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View
                            Project</span>
                    </a>
                    <a :href="alpineCaseStudy" target="_blank"
                        class="w-full sm:w-auto px-6 md:px-7 lg:px-10 py-3 rounded-full relative group flex justify-center">
                        <span
                            class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-dark font-medium">View Case
                            Study</span>
                    </a>
                </div>
            </div>
        </section>

    </main>
    <FooterSection id="contact" />
</template>