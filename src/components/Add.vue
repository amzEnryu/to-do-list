<template>
    <div>
        <form class="" @submit.prevent="addItem">
            <label for="new-item-input">New Item</label>
            <div class="form-group d-flex justify-content-center align-items-center">
                <input type="text" class="form-control" id="new-item-input" placeholder="Add the new one you want"
                    v-model="newItemText">
                <button type="submit" class="btn btn-primary">Add Item</button>
            </div>

        </form>
    </div>
</template>
  
<script>
export default {
    name: 'Add',
    data() {
        return {
            newItemText: ''
        }
    },
    methods: {
        addItem() {
            if (this.newItemText.trim() === '') {
                return;
            }

            const newItem = {
                title: this.newItemText,
                completed: false
            };

            this.$emit('new-item-added', newItem);
            this.newItemText = '';
        }
    }
}
</script>
<style scoped>
form {
    flex-direction: column;
}
</style>
  