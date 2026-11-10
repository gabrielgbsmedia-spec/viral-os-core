<script setup lang="ts">
withDefaults(
    defineProps<{
        variant?: 'full' | 'mark';
    }>(),
    { variant: 'full' },
);
</script>

<template>
    <span
        class="inline-flex shrink-0 items-center gap-[0.42em] font-logo leading-none font-bold tracking-[-0.02em] text-foreground"
        role="img"
        aria-label="ViralOS"
        data-testid="app-logo"
    >
        <svg
            viewBox="0 0 40 40"
            class="size-[1.2em] shrink-0"
            aria-hidden="true"
        >
            <defs>
                <linearGradient id="viralos-gradient" x1="4" y1="4" x2="36" y2="36">
                    <stop offset="0%" stop-color="#7C3AED" />
                    <stop offset="55%" stop-color="#4F46E5" />
                    <stop offset="100%" stop-color="#06B6D4" />
                </linearGradient>
            </defs>
            <rect x="2" y="2" width="36" height="36" rx="11" fill="url(#viralos-gradient)" />
            <path
                d="M10.5 12.5L18.2 28H21.8L29.5 12.5H25.1L20 23.4L14.9 12.5H10.5Z"
                fill="white"
            />
        </svg>
        <span v-if="variant === 'full'" aria-hidden="true">ViralOS</span>
    </span>
</template>
