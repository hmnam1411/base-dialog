<template>
    <BaseDialog v-bind="$attrs" v-on="$listeners">
        <div class="title" slot="title">
            Đây là title
        </div>
        <div class="dialog-body">
            Content ở đây
        </div>

        <div class="footer" slot="footer">
            <button type="button" @click="$emit('update:active', false)">Ok</button>
        </div>
    </BaseDialog>
</template>
  
<script>
import BaseDialog from "../BaseDialog.vue";

export default {
    name: "AlertDialog",
    components: {
        BaseDialog
    },
    props: {
        title: String,
        content: String,
        confirmText: {
            type: String,
            default: "Ok"
        }
    }
};
</script>
  
<style scoped>




.dialog-footer button {
    padding: 5px 10px;
    font-size: 16px;
    cursor: pointer;
}
</style>
  