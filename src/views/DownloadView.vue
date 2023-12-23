<template>
    <div class='w-full p-5'>
      <div class='max-w-5xl dark:text-white centerbox text-center'>
        <h1 class='font-bold text-2xl mb-5'>Installation for Minecraft Launcher</h1>
        <p class='text-center'>The Minecraft and Flint Loader versions can be selected in the installer, this download works for every version we support.</p>

        <div class='w-full text-center mt-5'>
          <a :href='dlLink' class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-white rounded-lg bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-900">
            Download Flint Installer ({{ version }})
            <svg class="w-3.5 h-3.5 ms-2 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
            </svg>
          </a>
          <br />
          <br />
          <p class='text-sm'>Most modules will also require the <a href='https://maven.flintloader.net/#/releases/net/flintloader/flint-api' class='text-blue-500'>Flint API</a> which needs to be placed in the modules folder</p>
          <br />
          <br />
          <h1 class='font-bold text-2xl mb-5'>Installation Instructions</h1>

          <ul class='text-left'>
            <li>• Download the Flint Installer from above.</li>
            <li>• Open the installer. In the window you can select the Minecraft version, loader version (latest recommended), and the install location (default recommended).</li>
            <li>• To show snapshots in the Minecraft versions dropdown, tick the 'Show Snapshots' checkbox</li>
            <li>• The install location is the location of Minecraft Launcher. If you want to change your instance's directory use Minecraft Launcher's instance options</li>
            <li>• Press Install. A new game version and profile will be created in the launcher's menu, which you can now use to launch Flint.</li>
            <li>• You may then want to launch your newly created instance once, and then add Flint API to your instance's modules folder as most mods will need it</li>
          </ul>
        </div>
      </div>
    </div>
</template>

<script setup lang='ts'>

import { onMounted, ref } from 'vue'

const dlLink = ref("#");
const version = ref("Loading");

onMounted(async () => {
  fetch("https://meta.flintloader.net/v1/versions/installer").then(async res => {
    const data = await res.json() as any

    if (data) {
      dlLink.value = data[0].url;
      version.value = data[0].version;
    }
  })
})

</script>