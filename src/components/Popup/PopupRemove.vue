<template>
  <BaseDialogVue v-bind="$attrs" v-on="$listeners">
        <div class="title" slot="title">
            Title Popup Remove
        </div>
        
        <div class="content">
            Content Popup Remove
        </div>

        <div class="footer" slot="footer">
            <button type="button" @click="$emit('update:active', false)">Ok Remove</button>
        </div>
    </BaseDialogVue>
</template>

<script>
import BaseDialogVue from '../BaseDialog.vue'
export default {
    components: {
        BaseDialogVue
    }
}
</script>

<style>

</style>