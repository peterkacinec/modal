<template>
    <div class="modal fade" id="modalConfirm" data-backdrop="static" data-keyboard="false" tabindex="-1" role="dialog" aria-labelledby="staticBackdropLabel" aria-hidden="true">
        <div class="modal-dialog" role="document">
            <form ref="form" id="deleteForm" method="post" :action="this.config.url">
                <input type="hidden" name="_method" value="DELETE">
                <input type="hidden" name="_token" :value="csrf">
                <div class="modal-content">
                    <div class="modal-body">
                        <p class="text-center">{{ this.config.modalText }}</p>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                        <button type="submit" data-dismiss="modal" class="btn btn-danger" @click="submit">Yes</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['config'],
        data() {
            return {
                csrf: document.querySelector('meta[name="csrf-token"]').getAttribute('content'),
            };
        },
        methods: {
            submit() {
                this.$refs.form.submit()
            }
        }
    };
</script>
