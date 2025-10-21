<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                // newItem: ""
            }
            
        },
        methods: {
            remove(index) {
                this.items.splice(index, 1)
            },
            add(element){
                this.items.push(element)

            }
        }
    }
    
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
    <li v-for="(item, index) in items">{{item}} <button @click="remove(index)">Delete!</button></li>
    </ul>

    <input v-model="newItem"></input>  
    <button  @click="add(newItem)">Add</button>
</template>
