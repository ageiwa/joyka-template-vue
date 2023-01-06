<script setup>
    import './style.scss'
    const props = defineProps({
        title: String,
        showIcon: Boolean
    })
</script>

<template>
    <button class="send-joyka-btn" type="button">
        {{ title }}
        <span v-if="showIcon" class="send-joyka-btn__icon-wrap">
            <img class="send-joyka-btn__icon" src="@/assets/preview-btn-submit.png">
        </span>
    </button>
</template>