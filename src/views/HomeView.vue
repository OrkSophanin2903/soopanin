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
    <div class="flex flex-col gap-2">
      <div class="text-3xl font-bold">sophanin ork</div>
      <div class="text-sm text-gray-700">outdoor, coding, running, athlete, and officer</div>
    </div>

    <div class="text-sm gap-2 flex flex-col">
      <div class="flex gap-x-1">
        <span class="font-bold">currently:</span>
        <span class="text-gray-700">senior hrms developer</span>
      </div>
      <div class="flex gap-x-1">
        <span class="font-bold">location:</span>
        <span class="text-gray-700">Phnom Penh, Cambodia</span>
        <span class="text-gray-700"
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

    <div class="flex flex-col gap-2 text-sm">
      <CommonLink to="/careers">careers</CommonLink>
      <CommonLink to="/projects">projects</CommonLink>
      <CommonLink to="/projects">resume</CommonLink>
    </div>

    <div class="flex flex-col gap-4">
      <a
        href="mailto:sophanin11t@gmail.com"
        class="w-fit text-sm text-gray-700 hover:text-gray-950 transition-opacity duration-300"
      >
        sophanin11t@gmail.com
      </a>

      <div class="flex gap-x-4">
        <CommonSocialLink
          href="https://www.linkedin.com/in/sophanin-ork-956b671ba"
          label="LinkedIn"
          color="#0A66C2"
        >
          <LinkedinIcon />
        </CommonSocialLink>
        <CommonSocialLink href="https://github.com/OrkSophanin2903" label="GitHub" color="#181717">
          <GithubIcon />
        </CommonSocialLink>
        <CommonSocialLink href="https://x.com/nin81157456" label="X" color="#000000">
          <XIcon />
        </CommonSocialLink>
        <CommonSocialLink
          href="https://www.strava.com/athletes/153258611"
          label="Strava"
          color="#FC4C02"
        >
          <StravaIcon />
        </CommonSocialLink>
      </div>
    </div>
  </div>
</template>
