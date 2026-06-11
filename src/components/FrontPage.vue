<script setup lang="ts">
import ProjectCard from './ProjectCard.vue';
import ItchIoIcon from './icons/ItchIoIcon.vue';
import LinkedInIcon from './icons/LinkedInIcon.vue';
function scrollTo(id : string) {
    const element = document.getElementById(id);
    if (element) {
        const header = document.getElementById('header');
        // element.scrollIntoView({ behavior: 'smooth' });
        const yOffset = header ? -header.offsetHeight : 0;
        const y = element.getBoundingClientRect().top + window.scrollY + yOffset;

        window.scrollTo({top: y, behavior: 'smooth'});
    }
}
</script>

<template>
    <div class="flex flex-col items-center bg-linear-to-r from-slate-950 to-zinc-950">
        <header class="max-w-7xl w-full sm:px-14 px-8 fixed flex flex-col gap-2 bg-linear-to-r from-slate-950 to-zinc-950 z-10 pt-8 pb-4" id="header">
            <div class="relative w-full border-b-2 border-white pb-4">
                <h1 class="text-white md:text-4xl sm:text-3xl text-2xl font-bold">Birk Lerviks <span class="text-zinc-500 mx-2">\</span> <a href="index.html">Game Developer Portfolio</a></h1>
            </div>
            <div class="flex text-zinc-500 md:text-base text-sm font-bold pt-2 uppercase flex gap-6 lg:px-4">
                <button class="cursor-pointer hover:text-white" @click="scrollTo('about')">About</button>
                <button class="cursor-pointer hover:text-white" @click="scrollTo('projects')">Projects</button>
                <button class="cursor-pointer hover:text-white" @click="scrollTo('contact')">Contact</button>
                <div class="ml-auto flex flex-row gap-4">
                    <a href="https://www.linkedin.com/in/birk-lerviks-12450526a/" target="_blank">
                        <LinkedInIcon class="scale-125"/>
                    </a>
                    <a href="https://birklerviks.itch.io/" target="_blank">
                        <ItchIoIcon class="scale-125"/>
                    </a>
                </div>
            </div>
        </header>
        <main class="flex flex-col w-full items-center pt-37">
            <div class="max-w-7xl w-full sm:px-14 px-8 text-white pb-20">
                <div class="pt-6">
                    <div class="flex gap-8 sm:pt-4" id="about">
                        <div class="flex flex-col gap-4 text-zinc-300">
                            <h2 class="sm:text-4xl text-2xl font-bold">About</h2>
                            <div class="flex flex-col gap-4 lg:pl-4 relative md:text-left sm:text-justify">
                                <div>
                                    <img src="/headshot.jpg" class="float-right md:hidden block w-32 h-32 object-cover zoom scale rounded-full m-4 -mt-12">
                                    <p class="text-pretty">Hi! I'm a game developer interested in both designing gameplay experiences and building the tech that makes them possible, whether that's developing game mechanics, crafting worlds, or doing deep dives into rendering and performance.</p>
                                </div>
                                <p>I've worked in multidisciplinary teams as a designer, programmer, and producer, taking ideas from original concept to fully playable experiences. I'm especially interested in how gameplay, narrative, and technical execution come together to create cohesive player experiences.</p>
                                <p>I also have experience in web development and customer support, giving me a strong understanding of both technical implementation and user-facing products.</p>
                                <p>Beyond game development, I bring a creative background in theater and music, which influences how I approach pacing, storytelling, and player immersion.</p>
                                <p>You'll find detailed breakdowns of my contributions in various projects below.</p>
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
                                    <p>Vue</p>
                                    <p>React</p>
                                    <p>Unreal Engine Blueprints</p>
                                    <p>Shader Graph</p>
                                </div>
                            </div>
                            <div class="flex flex-col gap-2 mt-4">
                                <p class="text-2xl font-bold text-white">Programming</p>
                                <div class="flex flex-wrap gap-x-4 gap-y-2 lg:pl-4">
                                    <p>C++</p>
                                    <p>C#</p>
                                    <p>GLSL</p>
                                    <p>HLSL</p>
                                    <p>Compute Shaders</p>
                                    <p>Python</p>
                                    <p>GDScript</p>
                                    <p>Javascript</p>
                                    <p>Java</p>
                                    <p>HTML</p>
                                    <p>CSS</p>
                                    <p>Scala</p>
                                </div>
                            </div>
                        </div>
                        <div class="w-260 md:block hidden lg:mr-4">
                            <img src="/headshot.jpg" class="rounded-lg">
                        </div>
                    </div>
                </div>
                <div class="pt-16 -mb-20">
                    <h2 class="sm:text-4xl text-2xl font-bold mb-4 pt-4" id="projects">Select Projects</h2>
                    <div class="w-full border-b-2 border-white mb-4"></div>
                    <div class="hidden sm:flex flex-wrap text-zinc-500 md:text-base text-sm font-bold uppercase flex gap-6 px-4">
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('frostbite')">Frostbite</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('aris-arcanum')">Aris Arcanum</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('planet-shader')">Planet Shader</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('conscience')">Conscience</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('witchs-brew')">Witch's Brew</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('the-unfortunates')">The Unfortunates</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('dungeons-and-chatbots')">Dungeons and Chatbots</button>
                        <button class="cursor-pointer hover:text-white" @click="scrollTo('kahoot-sparks')">Kahoot! Sparks</button>
                    </div>
                    <div class="flex flex-col sm:mt-8">
                        <project-card :flip="true" id="frostbite">
                            <template #header>Volumetric Temporal Anti-Aliasing at Frostbite</template>
                            <template #description>
                                <p><b>Role:</b> Master's Thesis Intern</p>
                                <p><b>Company: </b> Frostbite (Electronic Arts)</p>
                                <p><b>Duration:</b> 6 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Improved the volumetric rendering capabilities of the Frostbite engine</li>
                                    <li>Developed and implemented novel temporal anti-aliasing techniques for volumetric rendering, enabling high-quality dynamic volumetric lighting</li>
                                    <li>Working with cutting-edge rendering methods in a production engine environment</li>
                                </ul>
                                <p><b>Engines and tools:</b> Frostbite, C++, HLSL</p>
                            </template>
                            <template #content>
                                <iframe width="560" height="315" src="https://www.youtube.com/embed/wKfzuX3TBG0?si=PBjiXIAWEkoKwCWg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                            </template>
                        </project-card>
                        <project-card :flip="false" id="aris-arcanum">
                            <template #header>Aris Arcanum (PC, Steam)</template>
                            <template #description>
                                <p><b>Role:</b> Gameplay Designer, Programmer</p>
                                <p><b>Company: </b> Broken Cane</p>
                                <p><b>Team size:</b> 7 | <b>Duration:</b> 12 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Designed two boss fights and implemented them in Unity using C#</li>
                                    <li>Built supporting gameplay systems and integrated controller support</li>
                                    <li>Iterated on combat flow based on playtesting and player feedback</li>
                                </ul>
                                <p><b>Engines and tools:</b> Unity, C#</p>
                                <p>Check out the project on <a href="https://store.steampowered.com/app/3006080/Aris_Arcanum/" target="_blank" class="underline hover:underline">Steam</a></p>
                            </template>
                            <template #content>
                                <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/VQCOLdqp_Lw?si=XDMZWmjq_s5uqyms" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                            </template>
                        </project-card>
                        <project-card :flip="true" id="conscience">
                            <template #header>Conscience (PC, Itch.io)</template>
                            <template #description>
                                <p><b>Role:</b> Project Lead, Designer & Programmer</p>
                                <p><b>Team size:</b> 7 | <b>Duration:</b> 3 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Created the original concept, and defined game direction, scope, and production priorities throughout development</li>
                                    <li>Led development from concept to playable release, coordinating a multidisciplinary team</li>
                                    <li>Designed and implemented core gameplay systems and interaction mechanics in Unreal Engine using Blueprints and C++</li>
                                    <li>Created a modular architecture system and created most of the 3D art assets in Blender, also some 2D assets in Photoshop</li>
                                    <li>Worked closely with narrative and audio to align tone and player experience</li>
                                </ul>
                                <p><b>Engines and tools:</b> Unreal Engine, Blueprints, C++, Blender, Photoshop</p>
                                <p>Check out the project on <a href="https://birklerviks.itch.io/conscience" target="_blank" class="underline hover:underline">itch.io</a></p>
                            </template>
                            <template #content>
                                <iframe class="w-full h-full object-cover" title="vimeo-player" src="https://player.vimeo.com/video/799027301?h=34c43446b3" width="640" height="360" frameborder="0" referrerpolicy="strict-origin-when-cross-origin" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share"   allowfullscreen></iframe>
                            </template>
                        </project-card>
                        <project-card :flip="false" id="witchs-brew">
                            <template #header>Witch's Brew (PC, Itch.io)</template>
                            <template #description>
                                <p><b>Role:</b> Project Lead, Designer & Programmer</p>
                                <p><b>Team size:</b> 8 | <b>Duration:</b> 3 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Created the original concept, and defined game direction, scope, and production priorities throughout development</li>
                                    <li>Directed development of the 3D exploration / adventure experience from early concept to playable game</li>
                                    <li>Designed and implemented gameplay systems for exploration, dialogue, inventory management, and potion crafting in Unity using C# and Yarn Spinner</li>
                                    <li>Balanced scope and features to maintain a cohesive player experience, especially important given the limited development time</li>
                                </ul>
                                <p><b>Engines and tools:</b> Unity, C#</p>
                                <p>Check out the project on <a href="https://jintastic.itch.io/witchs-brew" target="_blank" class="underline hover:underline">itch.io</a></p>
                            </template>
                            <template #content>
                                <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/hm6OkGk7Hik?si=LRRmymiygBCP7K7n" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                            </template>
                        </project-card>
                        <project-card :flip="true" id="planet-shader">
                            <template #header>Volumetric Planet Shader (PC)</template>
                            <template #description>
                                <p><b>Role:</b> Graphics Programmer</p>
                                <p><b>Team size:</b> 2 | <b>Duration:</b> 2 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Built a full procedural planet generation and rendering pipeline from scratch</li>
                                    <li>Implemented compute shader–based terrain generation</li>
                                    <li>Developed volumetric atmosphere and cloud rendering using ray marching</li>
                                    <li>Combined physically inspired lighting with stylized visual direction</li>
                                    <li>Optimized both planet generation and volumetric rendering to run in real-time on modern hardware</li>
                                </ul>
                                <p><b>Engines and tools:</b> GLSL, C++, ImGui</p>
                            </template>
                            <template #content>
                                <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/LwNbftrN8QU?si=qbzwRHfs4QShov8v" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                            </template>
                        </project-card>
                        <project-card :flip="false" id="dungeons-and-chatbots">
                            <template #header>Dungeons and Chatbots (PC)</template>
                            <template #description>
                                <p><b>Role:</b> Gameplay Designer & Systems Programmer</p>
                                <p><b>Team size:</b> 4 | <b>Duration:</b> 2 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Implemented real-time generative AI systems driving dynamic game content, supporting text, images, and audio</li>
                                    <li>Integrated AI pipelines into the game engine for runtime world generation</li>
                                    <li>Designed and built core gameplay systems, including a robust save/load system</li>
                                    <li>Explored design implications of generative AI-driven gameplay, focusing on player agency, immersion, and narrative coherence</li>
                                </ul>
                                <p><b>Engines and tools:</b> Unity, C#, Gemini</p>
                            </template>
                            <template #content>
                                <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/1imfNe6lKvU?si=NQdYZCY33Mr3xPc9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                            </template>
                        </project-card>
                        <project-card :flip="true" id="the-unfortunates">
                            <template #header>The Unfortunates (PC, Itch.io)</template>
                            <template #description>
                                <p><b>Role:</b> Gameplay Designer & Programmer</p>
                                <p><b>Team size:</b> 7 | <b>Duration:</b> 2 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Designed and implemented multiple gameplay systems, focusing on their utility for narrative progression</li>
                                    <li>Helped shape narrative structure and pacing of the experience</li>
                                    <li>Collaborated closely with team to align gameplay and storytelling</li>
                                </ul>
                                <p><b>Engines and tools:</b> Unity, C#</p>
                                <p>Check out The Unfortunates on <a href="https://birklerviks.itch.io/the-unfortunates" target="_blank" class="underline hover:underline">itch.io</a></p>
                            </template>
                            <template #content>
                                <img class="w-full h-full object-cover" src="https://img.itch.zone/aW1hZ2UvNDAzMjI1NS8yNDAzOTc3MC5qcGc=/original/gVGB8t.jpg">
                            </template>
                        </project-card>
                        <project-card :flip="false" id="kahoot-sparks">
                            <template #header>Kahoot! Sparks (Web)</template>
                            <template #description>
                                <p><b>Role:</b> Frontend Developer</p>
                                <p><b>Company: </b>Whiteboard.fi, a Kahoot! company</p>
                                <p><b>Team size:</b> 8 | <b>Duration:</b> 6 months</p>
                                <p><b>My contributions:</b></p>
                                <ul class="list-disc list-outside ml-8">
                                    <li>Developed core functionality for a gamified learning platform (edutainment)</li>
                                    <li>Built responsive UI components in close collaboration with design teams</li>
                                    <li>Worked with production systems in a live product environment</li>
                                </ul>
                                <p><b>Engines and tools:</b> JavaScript, HTML, CSS, Vue, TailwindCSS, Figma</p>
                            </template>
                            <template #content>
                                <iframe class="w-full h-full object-cover" width="560" height="315" src="https://www.youtube.com/embed/rarrXMD74qo?si=mPEqxhwhFhsUJmBV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                            </template>
                        </project-card>
                    </div>
                </div>
                <div class="pt-16">
                    <h2 class="sm:text-4xl text-2xl font-bold mb-4 pt-4" id="contact">Contact</h2>
                    <div class="w-full border-b-2 border-white mb-4"></div>
                    <p class="text-zinc-300">Please feel free to reach out if you want to play some pinball or if you're interested in working together!</p>
                    <p class="text-zinc-300 mt-4"><u>birklerviks@gmail.com</u></p>
                    <div class="flex flex-row mt-6 gap-4 pl-0.5">
                        <a href="https://www.linkedin.com/in/birk-lerviks-12450526a/" target="_blank">
                            <LinkedInIcon class="scale-125"/>
                        </a>
                        <a href="https://birklerviks.itch.io/" target="_blank">
                            <ItchIoIcon class="scale-125"/>
                        </a>
                    </div>
                </div>
            </div>
            <footer class="w-full py-10 flex items-center justify-center text-center text-zinc-500 bg-black">
                <p>Copyright © 2026 Birk Lerviks. <br class="sm:hidden"> All rights reserved.</p>
            </footer>
        </main>
    </div>
</template>