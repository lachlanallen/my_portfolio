<script setup>
import { ref } from 'vue';
const Menu = ref([
    { name: 'About', link: '#about' },
    { name: 'Skills', link: '#skills' },
    { name: 'Projects', link: '#projects' },
    { name: 'Contact', link: '#contact' }
]);

const isMenuOpen = ref(false);
const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
    }
};
</script>

<template>
    <header class="flex justify-between items-center p-6 bg-opacity-50 relative z-20 font-sans-serif">
        <div class="text-primary text-3xl font-bold">Portfolio</div>
        <!-- Mobile Toggle Button -->
        <div class="md:hidden z-30">
            <button type="button" class="block focus:outline-none" 
            @click="isMenuOpen = !isMenuOpen">
                <span v-if="isMenuOpen" class="text-5xl">
                    <img src="@/assets/x.svg" alt="close" width="48"
                        height="48" />
                </span>
                <span v-else class="text-5xl">
                    <img src="@/assets/menu.svg" alt="menu" width="48"
                        height="48" />
                </span>
            </button>
        </div>
        <!-- Navigation Links -->
        <nav :class="['fixed inset-0 z-20 flex flex-col items-center justify-center bg-light md:relative md:bg-transparent md:flex md:justify-between md:flex-row', isMenuOpen ? 'block' : 'hidden']">
            <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                <li v-for="item in Menu" :key="item.name">
                    <a :href="item.href"
                        class="text-primary transition hover:text-tertiary ease-linear text-2xl md:text-lg"
                        @click="scrollToSection(item.href)">
                        {{ item.name }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>