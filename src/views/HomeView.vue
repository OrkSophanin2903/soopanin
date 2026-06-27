<script setup lang="ts">
import CommonLink from "@/components/CommonLink.vue";
import CommonSocialLink from "@/components/CommonSocialLink.vue";
import LinkedinIcon from "@/components/icons/LinkedinIcon.vue";
import GithubIcon from "@/components/icons/GithubIcon.vue";
import XIcon from "@/components/icons/XIcon.vue";
import StravaIcon from "@/components/icons/StravaIcon.vue";
import { onMounted } from "vue";

onMounted(() => {
  const script = document.createElement("script");
  script.src = "//w.24timezones.com/l.js";
  script.async = true;
  document.body.appendChild(script);
});
</script>

<template>
  <div class="flex flex-col gap-8">
    <div class="flex flex-col gap-1">
      <div class="text-2xl font-bold">sophanin ork</div>
      <div class="text-xs text-gray-500">outdoor, coding, running, athlete, and officer</div>
    </div>

    <div class="text-xs gap-2 flex flex-col">
      <div class="flex gap-x-1">
        <span class="font-bold">currently:</span>
        <span class="text-gray-500">senior hrms developer</span>
      </div>
      <div class="flex gap-x-1">
        <span class="font-bold">location:</span>
        <span class="text-gray-500">Phnom Penh, Cambodia</span>
        <span class="text-gray-500"
          ><a
            href="//24timezones.com/Phnom-Penh/time"
            style="text-decoration: none"
            class="clock24"
            id="tz24-1782568492-c1199-eyJob3VydHlwZSI6MTIsInNob3dkYXRlIjoiMCIsInNob3dzZWNvbmRzIjoiMSIsInNob3d0aW1lem9uZSI6IjEiLCJ0eXBlIjoiZCIsImxhbmciOiJlbiJ9"
            title="World Clock :: Phnom Penh"
            target="_blank"
            rel="nofollow"
          >
          </a
        ></span>
      </div>
    </div>

    <div class="flex flex-col gap-2 text-xs">
      <CommonLink to="/careers">careers</CommonLink>
      <CommonLink to="/projects">projects</CommonLink>
    </div>

    <div class="flex flex-col gap-3">
      <a
        href="mailto:sophanin11t@gmail.com"
        class="w-fit text-xs text-gray-500 hover:text-gray-950 transition-opacity duration-300"
      >
        sophanin11t@gmail.com
      </a>

      <div class="flex gap-x-4">
        <CommonSocialLink
          href="https://www.linkedin.com/in/USERNAME"
          label="LinkedIn"
          color="#0A66C2"
        >
          <LinkedinIcon />
        </CommonSocialLink>
        <CommonSocialLink href="https://github.com/USERNAME" label="GitHub" color="#181717">
          <GithubIcon />
        </CommonSocialLink>
        <CommonSocialLink href="https://x.com/USERNAME" label="X" color="#000000">
          <XIcon />
        </CommonSocialLink>
        <CommonSocialLink
          href="https://www.strava.com/athletes/USERNAME"
          label="Strava"
          color="#FC4C02"
        >
          <StravaIcon />
        </CommonSocialLink>
      </div>
    </div>
  </div>
</template>
