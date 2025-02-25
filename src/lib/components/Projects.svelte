<script lang="ts">
  import projects from '$lib/data/projects.json';
  import type { ComponentType } from 'svelte';
  import FirebaseIcon from './icons/FirebaseIcon.svelte';
  import GithubIcon from './icons/GithubIcon.svelte';
  import LinkIcon from './icons/LinkIcon.svelte';
  import NextjsIcon from './icons/NextjsIcon.svelte';
  import ReactIcon from './icons/ReactIcon.svelte';
  import TailwindcssIcon from './icons/TailwindcssIcon.svelte';
  import TypescriptIcon from './icons/TypescriptIcon.svelte';

  const iconComponents: Record<string, ComponentType> = {
    React: ReactIcon,
    Nextjs: NextjsIcon,
    Typescript: TypescriptIcon,
    Firebase: FirebaseIcon,
    Tailwindcss: TailwindcssIcon,
  };
</script>

<section class="mt-8 lg:mt-16">
  <h2 class="font-bold text-2xl">Projects</h2>

  {#each projects as project}
    <div class="my-6 xs:flex xs:flex-row xs:w-full xs:gap-6">
      <a href={project.link} target="_blank">
        <img class="w-full xs:w-auto h-52 rounded-xl " src={project.image} alt="" />
      </a>
      <div class="flex items-start gap-6 mt-4 ">
        <div class="w-12 h-12 p-1 shrink-0 xs:hidden rounded-full border border-antiflashWhite ">
          <img class="w-full h-full" src={project.icon} alt="" />
        </div>
        <div class="max-w-72">
          <h3 class="font-bold text-lg">{project.title}</h3>
          <h3 class="text-lg">{project.sub_title}</h3>
          <p class="text-sm py-2">{project.description}</p>
          <div class="flex flex-wrap items-center space-x-2 gap-1.5">
            {#each project.tecnologies as tech}
              {#if iconComponents[tech]}
                <div
                  class="flex items-center space-x-1 rounded-2xl border border-antiflashWhite p-1 px-2"
                >
                  <svelte:component
                    this={iconComponents[tech]}
                    customClasses={'w-4 h-4'}
                  />
                  <span class="text-xs font-semibold">{tech}</span>
                </div>
              {/if}
            {/each}
          </div>

          <div class="flex items-center space-x-4 mt-2">
            <a href={project.link} target="_blank">
              <LinkIcon />
            </a>
            <a href={project.github} target="_blank">
              <GithubIcon />
            </a>
          </div>
        </div>
        <div class="hidden w-12 h-12 p-1 shrink-0 xs:block rounded-full border border-antiflashWhite ">
          <img class="w-full h-full" src={project.icon} alt="" />
        </div>
      </div>
    </div>
  {/each}
</section>
