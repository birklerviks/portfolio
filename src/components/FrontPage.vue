<script setup la
  components: { ProjectCard },ng="ts">
import ProjectCard from './ProjectCard.vue';
import ItchIoIcon from './icons/ItchIoIcon.vue';
import SteamIcon from './icons/SteamIcon.vue';
function scrollTo(id) {
    const element = document.getElementById(id);
    if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
    }
}
</script>

<template>
    <div class="w-full bg-linear-to-r from-slate-950 to-zinc-950 md:px-24 sm:px-14 px-8 pt-16 text-white pb-20">
        <div class="w-full flex flex-col gap-2">
            <div class="relative w-full border-b-2 border-white pb-4">
                <h1 class="text-white md:text-4xl text-3xl font-bold">Birk Lerviks <span class="text-zinc-500 mx-2">\</span> <a href="index.html">Game Developer Portfolio</a></h1>
                <div class="absolute right-4 -bottom-10">
                    
                </div>
            </div>
            <div class="flex text-zinc-500 md:text-base text-sm font-bold pt-2 uppercase">
                <button class="cursor-pointer px-4 hover:text-white" @click="scrollTo('about')">About</button>
                <button class="cursor-pointer px-4 hover:text-white" @click="scrollTo('projects')">Projects</button>
                <button class="cursor-pointer px-4 hover:text-white" @click="scrollTo('contact')">Contact</button>
                <a href="https://birklerviks.itch.io/" target="_blank" class="gap-2 mr-4 ml-auto">
                    <ItchIoIcon class="scale-125"/>
                </a>
            </div>
        </div>
        <div class="pt-10" id="about">
            <h2 class="text-4xl font-bold mb-4">About</h2>
            <div class="flex gap-12">
                <div class="flex flex-col gap-4 text-zinc-300">
                    <div class="flex flex-col gap-4 lg:pl-4">
                        <p>Hi! I'm a game developer interested in both designing gameplay experiences and building the tech that makes them possible, whether that's designing mechanics, crafting worlds, or doing deep dives into rendering and performance.</p>
                        <p>At <i>Aalto University</i> in Helsinki, I worked on several game projects as producer, designer, and programmer. On <i>Conscience</i> and <i>Witch's Brew</i>, I led development while contributing to both game design and implementation, guiding mulitidisciplinary teams from initial concept to playable experience.</p>
                        <p>For <i>Aris Arcanum</i>, originally a university project, I designed and implemented two boss fights, focusing on gameplay feel, pacing, and how to convey the game's narrative and tone through gameplay.</p>
                        <p>At <i>Chalmers</i> and the <i>University of Gothenburg</i> I furthered my interest in game engine architecture and graphics programming. This led to my Master's thesis on Volumetric Temporal Anti-Aliasing together with Frostbite.</p>
                    </div>
                    <div class="flex flex-col gap-2 mt-4">
                        <p class="text-2xl font-bold text-white">Game Engines & Tools</p>
                        <div class="flex flex-wrap gap-x-4 gap-y-2 lg:pl-4">
                            <p>Unreal Engine</p>
                            <p>Unity</p>
                            <p>Godot</p>
                            <p>OpenGL</p>
                            <p>Vulkan</p>
                            <p>GitHub</p>
                            <p>Jira</p>
                            <p>Notion</p>
                        </div>
                    </div>
                    <div class="flex flex-col gap-2 mt-4">
                        <p class="text-2xl font-bold text-white">Programming</p>
                        <div class="flex flex-wrap gap-x-4 gap-y-2 lg:pl-4">
                            <p>C++</p>
                            <p>C#</p>
                            <p>GLSL</p>
                            <p>HLSL</p>
                            <p>Python</p>
                            <p>Javascript</p>
                            <p>HTML</p>
                            <p>CSS</p>
                            <p>Scala</p>
                        </div>
                    </div>
                </div>
                <div class="w-200 md:block hidden">
                    <img src="/public/headshot.jpg" class="rounded-lg brightness-90">
                </div>
            </div>
        </div>
        <div class="pt-20 -mb-20" id="projects">
            <h2 class="text-4xl font-bold mb-4">Projects</h2>
            <div class="w-full border-b-2 border-white mb-4"></div>
            <div class="hidden sm:flex flex-wrap text-zinc-500 md:text-base text-sm font-bold uppercase justify-center items-center">
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('frostbite')">Frostbite</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('aris-arcanum')">Aris Arcanum</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('planet-shader')">Planet Shader</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('conscience')">Conscience</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('witchs-brew')">Witch's Brew</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('the-unfortunates')">The Unfortunates</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('dungeons-and-chatbots')">Dungeons and Chatbots</button>
                <button class="cursor-pointer py-2 px-4 hover:text-white" @click="scrollTo('kahoot-sparks')">Kahoot! Sparks</button>
            </div>
        </div>
        <div class="flex flex-col mt-20">
            <project-card :flip="true" id="frostbite">
                <template #header>Master's Thesis Project at Frostbite</template>
                <template #description>
                    <p>I am currently working on my Master's Thesis at Frostbite.</p>
                    <p>As part of my research, I am implementing cutting-edge temporal anti-aliasing algorithms in a volumetric rendering context.</p>
                </template>
                <template #content>
                    <img class="w-full h-full object-cover" src="https://gameworldobserver.com/wp-content/uploads/2023/12/frostbite-rebrand-ea.jpg">
                </template>
            </project-card>
            <project-card :flip="false" id="aris-arcanum">
                <template #header>Aris Arcanum</template>
                <template #description>
                    <p>My biggest contribution to the game <i>Aris Arcanum</i> was designing and implementing the two boss fights. I also contributed with various gameplay systems and added controller support.</p>
                    <p>Check out the project on <a href="https://store.steampowered.com/app/3006080/Aris_Arcanum/" target="_blank" class="underline hover:underline">Steam</a></p>
                    <p><i>Engines and tools:</i> Unity, C#</p>
                    <p><i>Platforms: </i> PC</p>
                </template>
                <template #content>
                    <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/VQCOLdqp_Lw?si=XDMZWmjq_s5uqyms" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </template>
            </project-card>
            <project-card :flip="true" id="planet-shader">
                <template #header>Volumetric Planet Shader</template>
                <template #description>
                    <p>For this university project, I implemented the entire pipeline for generating, and rendering a stylized planet with realistic atmosphere and clouds.</p>
                    <p>The planet is procedurally generated in a compute shader and lit using a combination of ray marching and traditional lighting techniques.</p>
                    <p><i>Engines and tools:</i> GLSL, C++</p>
                </template>
                <template #content>
                    <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/LwNbftrN8QU?si=qbzwRHfs4QShov8v" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </template>
            </project-card>
            <project-card :flip="false" id="conscience">
                <template #header>Conscience</template>
                <template #description>
                    <p>Conscience is a short narrative-focused mystery horror game in which you explore a house to find out what happened to the family that lived there.</p>
                    <p>In this project I acted as project leader, responsible for the game direction and coordination of the 7-person development team. I also designed and implemented many of the game systems.</p>
                    <p>Check out the project on <a href="https://birklerviks.itch.io/conscience" target="_blank" class="underline hover:underline">itch.io</a></p>
                    <p><i>Engines and tools:</i> Unreal Engine, Blueprints, C++</p>
                    <p><i>Platforms:</i> PC</p>
                </template>
                <template #content>
                    <iframe class="w-full h-full object-cover" title="vimeo-player" src="https://player.vimeo.com/video/799027301?h=34c43446b3" width="640" height="360" frameborder="0" referrerpolicy="strict-origin-when-cross-origin" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share"   allowfullscreen></iframe>
                </template>
            </project-card>
            <project-card :flip="true" id="witchs-brew">
                <template #header>Witch's Brew</template>
                <template #description>
                    <p>This university project is a 3D exploration adventure where you find yourself stranded on a magical island and must find a way to escape.</p>
                    <p>In this project I acted as project leader, responsible for the game direction and coordination of the 8-person development team. I also designed and implemented many of the game systems.</p>
                    <p>Check out the project on <a href="https://jintastic.itch.io/witchs-brew" target="_blank" class="underline hover:underline">itch.io</a></p>
                    <p><i>Engines and tools:</i> Unity, C#</p>
                    <p><i>Platforms: </i> PC</p>
                </template>
                <template #content>
                    <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/hm6OkGk7Hik?si=LRRmymiygBCP7K7n" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </template>
            </project-card>
            <project-card :flip="false" id="the-unfortunates">
                <template #header>The Unfortunates</template>
                <template #description>
                    <p>In this narrative focused game you play the role of The Keeper, the spirit responsible for the branch of unfortunate souls, one of the many islands in the crossroads - the place before the afterlife.</p>
                    <p>My key contributions included designing and implementing various gameplay systems, and helping to define the narrative flow and structure.</p>
                    <p>Check out the project on <a href="https://birklerviks.itch.io/the-unfortunates" target="_blank" class="underline hover:underline">itch.io</a></p>
                    <p><i>Engines and tools:</i> Unity, C#</p>
                    <p><i>Platforms: </i> PC</p>
                </template>
                <template #content>
                    <img class="w-full h-full object-cover" src="https://img.itch.zone/aW1hZ2UvNDAzMjI1NS8yNDAzOTc3MC5qcGc=/original/gVGB8t.jpg">
                </template>
            </project-card>
            <project-card :flip="true" id="dungeons-and-chatbots">
                <template #header>Dungeons and Chatbots</template>
                <template #description>
                    <p>This university project explores how generative AI can be used in a real-time gameplay context. Everything in the game world is dynamically generated at runtime.</p>
                    <p>My key contributions included implementation of the AI generation systems and integration with the game engine, as well as the design and implementation of various gameplay systems such as a robust load and save system.</p>
                    <p><i>Engines and tools:</i> Unity, C#</p>
                    <p><i>Platforms: </i> PC</p>
                </template>
                <template #content>
                    <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/1imfNe6lKvU?si=NQdYZCY33Mr3xPc9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </template>
            </project-card>
            <project-card :flip="false" id="kahoot-sparks">
                <template #header>Kahoot! Sparks</template>
                <template #description>
                    <p>During my time at <a href="https://whiteboard.fi" target="_blank" class="underline hover:underline">Whiteboard.fi</a> I worked on various projects, including the development of gamified learning experiences such as Kahoot! Sparks.</p>
                    <p>My key contributions included implementing the core functionality and user interface for the Sparks platform, in close collaboration with the Kahoot! design and development team.</p>
                    <p><i>Engines and tools:</i> HTML, CSS, JavaScript</p>
                    <p><i>Platforms: </i> Web</p>
                </template>
                <template #content>
                    <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/rarrXMD74qo?si=mPEqxhwhFhsUJmBV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </template>
            </project-card>
        </div>
        <div class="pt-20" id="contact">
            <h2 class="text-4xl font-bold mb-4">Contact</h2>
            <div class="w-full border-b-2 border-white mb-4"></div>
            <p class="text-zinc-300">Please feel free to reach out if you want to chat about game development, or if you're interested in working together!</p>
            <p class="text-zinc-300 mt-4">birklerviks@gmail.com</p>
        </div>
    </div>
    <div class="py-10 text-center text-zinc-500 bg-black">
        <p>Copyright © 2026 Birk Lerviks. All rights reserved.</p>
    </div>
</template>