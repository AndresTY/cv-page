<template>
  <div class="networks">
    <IconLink 
      href="https://github.com/AndresTY" 
      icon="pi pi-github"
    />
    <IconLink 
      href="https://www.linkedin.com/public-profile/settings?trk=d_flagship3_profile_self_view_public_profile"
      icon="pi pi-linkedin"
    />
    <IconLink 
      href="https://www.twitch.tv/the_dukra"
      icon="pi pi-eye"
    />
  </div>
</template>

<script setup>
import IconLink from "@/components/atoms/IconLink.vue";
</script>

<style>
.networks{
    color: white;padding: 10%; display: inline;
}
</style>
