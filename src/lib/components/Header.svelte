<script lang="ts">
  import profileImage from '$lib/assets/profile_photo.jpg';
  import CvIcon from './icons/CvIcon.svelte';
  import GithubIcon from './icons/GithubIcon.svelte';
  import LinkedinIcon from './icons/LinkedinIcon.svelte';
</script>

<header class="mt-8 lg:mt-16">
  <div class="flex space-x-4 lg:space-x-6 items-center">
    <img
      class="w-32 h-32 sm:w-36 sm:h-36 rounded-full shadow-sm shadow-antiflashWhite"
      src={profileImage}
      alt="profile"
    />
    <div class="-mr-6">
      <h1 class="font-bold text-4xl">Yeraldi Mujica</h1>
      <h2 class="font-bold text-2xl mt-1">Fullstack Web Developer</h2>
      <p
        class="mt-2 text-xs w-fit font-semibold bg-amaranthPurple rounded-2xl py-1 px-2 text-center"
      >
        Open to remote opportunities
      </p>
      <div class="flex items-center space-x-4 mt-4">
        <CvIcon />
        <GithubIcon />
        <LinkedinIcon />
      </div>
    </div>
  </div>
  <section class="mt-6">
    <h2 class="font-bold text-2xl">About me</h2>
    <p class="mt-2">
      I'm a fullstack web developer and I always love facing new challenges that
      benefit me from knowledge and experience.
    </p>
  </section>
</header>
