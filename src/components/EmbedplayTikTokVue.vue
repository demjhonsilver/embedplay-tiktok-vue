<template>
    <div>
      <iframe 
        :src="playerUrl" 
        :height="height" 
        :width="width" 
        :style="{ border: 'none', borderRadius: formattedBorderRadius }" 
        allow="fullscreen" 
        title="TikTok Player"
      ></iframe>
    </div>
  </template>
  
  <script setup>
  import { computed } from 'vue';
  
  const props = defineProps({
    postId: {
      type: String,
      required: true
    },
    autoplay: {
      type: Boolean,
      default: false
    },
    controls: {
      type: Boolean,
      default: true
    },
    progressBar: {
      type: Boolean,
      default: true
    },
    playButton: {
      type: Boolean,
      default: true
    },
    volumeControl: {
      type: Boolean,
      default: true
    },
    fullscreenButton: {
      type: Boolean,
      default: true
    },
    timestamp: {
      type: Boolean,
      default: true
    },
    loop: {
      type: Boolean,
      default: false
    },
    musicInfo: {
      type: Boolean,
      default: false
    },
    description: {
      type: Boolean,
      default: false
    },
    rel: {
      type: Boolean,
      default: true
    },
    nativeContextMenu: {
      type: Boolean,
      default: true
    },
    width: {
      type: [Number, String],
      default: 400
    },
    height: {
      type: [Number, String],
      default: 300
    },
    borderRadius: {
    type: [Number, String],
    default: 0
    }
  });
  
  const playerUrl = computed(() => {
    const params = new URLSearchParams({
      autoplay: props.autoplay ? '1' : '0',
      controls: props.controls ? '1' : '0',
      progress_bar: props.progressBar ? '1' : '0',
      play_button: props.playButton ? '1' : '0',
      volume_control: props.volumeControl ? '1' : '0',
      fullscreen_button: props.fullscreenButton ? '1' : '0',
      timestamp: props.timestamp ? '1' : '0',
      loop: props.loop ? '1' : '0',
      music_info: props.musicInfo ? '1' : '0',
      description: props.description ? '1' : '0',
      rel: props.rel ? '1' : '0',
      native_context_menu: props.nativeContextMenu ? '1' : '0'
    }).toString();
    
    return `https://www.tiktok.com/player/v1/${props.postId}?${params}`;
  });
  
  const formattedBorderRadius = computed(() => {
  // Convert borderRadius to string with 'px' if it's a number
  return typeof props.borderRadius === 'number' ? `${props.borderRadius}px` : props.borderRadius;
  });
  </script>
  