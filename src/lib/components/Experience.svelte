<script lang="ts">
  import DeveloperIcon from './icons/DeveloperIcon.svelte';
  import FreelancerIcon from './icons/FreelancerIcon.svelte';
</script>

<section class="mt-8 lg:mt-16">
  <h2 class="font-bold text-2xl">Experience</h2>
  <div class="w-full">
    <ul class="">
      <li class="mt-6 mb-8 flex items-start space-x-6 max-w-lg">
        <DeveloperIcon customClasses="w-16 h-16" />
        <div class="max-w-60 sm:max-w-96">
          <h3 class="text-lg">Fullstack developer at LinkTIC</h3>
          <h4 class="text-sm font-semibold">August 13, 2023 - Current</h4>
          <p class="mt-4 text-sm">
            I have worked in several applications like virtual stores and
            systems, the technologies I have used has been sveltekit, supabase
            and in some cases laravel, I've been in contact with an AWS
            framework too called SST.
          </p>
        </div>
      </li>
      <li class="flex items-start space-x-6 max-w-lg">
        <FreelancerIcon customClasses="w-16 h-16" />
        <div class="max-w-60 sm:max-w-96">
          <h3 class="text-lg">Freelance Fullstack Developer</h3>
          <h4 class="text-sm font-semibold">
            February 01, 2023 - August 12, 2023
          </h4>
          <p class="mt-4">
            I worked doing several tasks in a admin panel made in laravel and I
            developed an admin panel for a client with laravel and mysql with a
            framework called Filamentphp, the admin panel has an inventory and
            several functions for the user and admin.
          </p>
        </div>
      </li>
    </ul>
  </div>
</section>
