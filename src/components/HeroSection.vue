<script setup>
import AOS from 'aos';
import 'aos/dist/aos';
AOS.init();
</script>

<template>
    <section class="relative w-full" data-aos="zoom-in-up">
        <div class="absolute top-0 inset-x-0 h-64 flex items-start">
            <div class="h-100 w-2/3 bg-gradient-to-br from-accent blur-2xl opacity-40"></div>
            <div class="h-100 w-3/5 bg-gradient-to-l from-secondary-accent blur-2xl opacity-40"></div>
        </div>
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg lg:max-w-screen-xl mx-auto relative">
            <div
                class="grid lg:grid-cols-2 gap-10 xl:gap-14 relative pt-24 lg:max-w-none max-w-2xl md:max-w 3xl mx-auto">
                <div class="lg:py-6">
                    <div class="text-center lg:text-left">
                        <h1 class="pt-4 text-primary font-bold font-serif text-4xl md:text-5xl lg:text-6xl">
                            Hi, I'm <span
                                class="text-transparent bg-clip-text bg-gradient-to-r from-accent-dark to-accent-darker">Lachlan
                            </span>₊˚⟡
                        </h1>
                    </div>
                    <p class="text-primary pt-8 text-center lg:text-left mx-auto max-w-xl">
                        I'm a passionate developer with a love for creating beautiful and functional web experiences.
                        Welcome to my portfolio!
                    </p>
                    <div class="flex items-center gap-3 pt-9 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
                        <button
                            class="px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
                            <span
                                class="absolute inset-0 rounded-3xl group-hover:scaale-105 origin-center transition-all ease-in-out bg-accent border-2 border-transparent"></span>
                            <span class="relative flex items-center justify-center text-dark font-medium">Hire Me</span>
                        </button>
                        <button
                            class="border border-accent-darker px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
                            <div
                                class="hover:scale-105 transition-all ease-in-out flex justify-center items-center relative">
                                <div class="svg-container">
                                    <img src="@/assets/download.svg" alt="download my resume" width="20" height="24" />
                                    <div class="download-loader text-primary hidden"></div>
                                </div>
                                <a href="/resume.pdf" download="/resume.pdf" class="pl-2 text-dark font-medium">Download
                                    Resume</a>
                            </div>
                        </button>
                    </div>
                </div>
                <div class="lg:h-full flex flex-col items-center justify-center sm:flex-col">
                    <div
                        class="flex w-full h-96 min-h-[24rem] lg:min-h-[none] lg:w-full lg:h-full items-center justify-center relative">
                        <div
                            class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-gradient-to-tr opacity-25 from-accent to-secondary-accent blur-2xl">
                        </div>
                        <div
                            class="absolute h-full z-10 p-2 -translate-y-1/2 top-1/2 lg:right-3 md:right-40 sm:right-0 sm:mx-auto rounded-full shadow-lg border border-primary">
                            <img src="@/assets/hero_image.jpg" alt="A woman sitting in a graduation gown" width="500"
                                height="auto" loading="lazy" class="w-full h-full rounded-full object-cover">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>