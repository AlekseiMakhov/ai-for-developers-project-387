<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { locale } = useI18n()
</script>

<template>
  <div class="flex items-center text-base sm:text-sm font-medium select-none">
    <button
      class="px-3 py-2 sm:px-1.5 sm:py-1 rounded transition-colors"
      :class="locale === 'ru' ? 'text-primary font-semibold' : 'text-muted-foreground hover:text-foreground'"
      @click="locale = 'ru'"
    >
      RU
    </button>
    <span class="text-muted-foreground/40 px-1 sm:px-0.5">|</span>
    <button
      class="px-3 py-2 sm:px-1.5 sm:py-1 rounded transition-colors"
      :class="locale === 'en' ? 'text-primary font-semibold' : 'text-muted-foreground hover:text-foreground'"
      @click="locale = 'en'"
    >
      EN
    </button>
  </div>
</template>
