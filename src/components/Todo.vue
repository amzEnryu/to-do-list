<template>
    <div>
        <Add @new-item-added="addItem"></Add>
        <div class='form-check' v-for="(list, index) in myJson.guest.list" :key="index">
            <div>
                <input class="form-check-input" type="checkbox" v-model="list.completed" :id="'checkbox-' + index" />
                <label :class="['form-check-label', list.completed ? 'completed' : 'abc']" :for="'checkbox-' + index">
                    {{ index + 1 }}. {{ list.title }}
                </label>
            </div>
            <button type="button" class="btn btn-danger" @click="deleteItem(index)">Delete</button>
        </div>
    </div>
</template>
    
<script>
import data from '../data.json'
import Add from './Add.vue'

export default {
    name: 'Todo',
    components: {
        Add
    },
    data() {
        return {
            myJson: data,
        }
    },
    methods: {
        deleteItem(index) {
            this.myJson.guest.list.splice(index, 1);
        },
        addItem(newItem) {
            this.myJson.guest.list.push(newItem);
        }
    }
}
</script>
  
<style scoped>
.form-check {
    background: #c1c1c1;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    margin: 10px;
    /* border: 1px #000; */
}

.completed {
    text-decoration: line-through;
}
</style>