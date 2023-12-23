<script setup lang="ts">

import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
import HomeJumbotron from '@/components/HomeJumbotron.vue'

onMounted(() => {
  initFlowbite()
})
</script>

<template>
  <main>
    <HomeJumbotron />

    <div class='w-full bg-white dark:bg-gray-900 p-5'>
      <hr class='mb-10 smallhr' />
      <div class='md:max-w-5xl w-full grid grid-cols-1 md:grid-cols-2 gap-5 centerbox'>
        <div class='dark:text-white'>
          <h1 class='font-bold text-2xl mb-2'>What is this?</h1>

          <p>
            Flint is a tiny, open-source modloader system, aimed at allowing developers to make client only mods, that players can use while playing on vanilla, paper/bukkit/spigot servers, without worrying about mod compatibility. <br /><br />
            We will also try to create our API in such a way that modules don't need to update with every single minecraft release. For now this project is a hobby side project, but if there is enough interest, it will be actively maintained and developed.
          </p>
        </div>

        <div>

          <div class="block max-w-sm p-6 bg-red-600 border border-red-200 rounded-lg shadow text-center dark:bg-red-900 dark:border-red-700 dark:text-white">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Alpha Notice</h5>
            <p class="font-normal">Flint is still in very early development, but is ready to be used for playing and developing modules on. Please report any issues or bugs you may find.</p>
          </div>

        </div>
      </div>

      <hr class='mt-10 smallhr' />

    </div>

    <div class='w-full bg-white dark:bg-gray-900 p-5'>
      <div class='max-w-5xl dark:text-white centerbox'>
        <h1 class='font-bold text-2xl mb-2'>Core Components</h1>

        <ul>
          <li>• <a href='https://github.com/FlintLoader/flint-punch' class='text-blue-500'>Flint Punch</a> The core, Version independent module loader for flint. This powers the core ecosystem</li>
          <li>• <a href='https://github.com/FlintLoader/flint-api' class='text-blue-500'>Flint API</a> Hooks and features for developing modules</li>
          <li>• <a href='https://github.com/FabricMC/yarn' class='text-blue-500'>Yarn</a> is a set of open Minecraft mappings, free for everyone to use under the Creative Commons Zero license.</li>
          <li>• <a href='https://github.com/FlintLoader/flint-steel' class='text-blue-500'>Flint Steel</a> A Gradle plugin enabling developers to easily develop and debug mods.</li>
          <li>• <a href='https://github.com/FabricMC/intermediary' class='text-blue-500'>Intermediary</a> contains match information between different versions of Minecraft, enabling cross version mods.</li>
          <li>• <a href='https://github.com/FabricMC/tiny-remapper' class='text-blue-500'>Tiny Remapper</a> A tiny, efficient tool for remapping JAR files.</li>
          <li>• <a href='https://github.com/FabricMC/mapping-io' class='text-blue-500'>Mapping IO</a> A library for reading, manipulating and writing mapping files, with support a wide range fo formats.</li>
        </ul>
      </div>

      <hr class='mt-10 smallhr' />
    </div>

    <div class='w-full bg-white dark:bg-gray-900 p-5 dark:text-white pb-10'>
      <p class='text-sm max-w-5xl centerbox text-center'>
        This project uses code and heavily modified components from the Fabric mod loader. It's not affiliated with or endorsed by either Fabric or Mojang Studios.<br /><br />
        This project is created and powered by <a href='https://firstdark.dev' class='text-blue-500'>First Dark Development</a>. &copy; 2023 Flint Loader Contributors
      </p>
    </div>
  </main>
</template>
