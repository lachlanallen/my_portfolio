<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter();

const Menu = ref([
    { name: 'About', link: '/' }, // Update link to just home route
    { name: 'Projects', link: '/projects' },
    { name: 'Contact', link: '#contact' } // Update link to just the hash
]);

const isMenuOpen = ref(false);

const handleClick = () => {
    isMenuOpen.value = false;
};

// Function to handle contact link click for smooth scrolling
const handleContactClick = (event) => {
    event.preventDefault(); // Prevent default hash jump
    const targetElement = document.querySelector('#contact');
    if (targetElement) {
        targetElement.scrollIntoView({ behavior: 'smooth' });
    }
    isMenuOpen.value = false; // Close menu after clicking
};

</script>

<template>
    <header class="flex justify-between items-center p-6 bg-opacity-50 relative z-20 font-sans-serif">
        <router-link to="/" class="text-primary text-3xl font-bold" @click="handleClick">Portfolio</router-link>
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
                    <!-- Conditional rendering/binding for Contact link -->
                    <a v-if="item.name === 'Contact'" :href="item.link"
                       class="text-primary transition hover:text-tertiary ease-linear text-2xl md:text-lg"
                       @click="handleContactClick">
                        {{ item.name }}
                    </a>
                    <!-- Use router-link for other links -->
                    <router-link v-else :to="item.link"
                        class="text-primary transition hover:text-tertiary ease-linear text-2xl md:text-lg"
                        @click="handleClick">
                        {{ item.name }}
                    </router-link>
                </li>
            </ul>
        </nav>
    </header>
</template>