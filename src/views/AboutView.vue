<template>

  <IframeRedirect/>

</template>
<script lang="ts">
import { Options,Vue } from "vue-class-component";
import IframeRedirect from '@/components/organisms/IframeRedirect.vue';

@Options({
  components: {
    IframeRedirect,
  },
})

export default class AboutView extends Vue {}
</script>