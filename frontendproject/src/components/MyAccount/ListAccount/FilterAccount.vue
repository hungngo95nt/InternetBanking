<template>
    <div class="divInput">
        <b-form-input
            type="text"
            placeholder="Tìm kiếm..."
            class="inputSearch"
            @keyup="handleChange($event)"
        ></b-form-input>
    </div>
</template>

<script>
export default {
    methods: {
        handleChange(event) {
            this.$store.dispatch("updateListAccountCustomer", event.target.value);
        }
    }
}
</script>

<style scoped>
.inputSearch{
    width: 100%;
}

.divInput{
    width: 300px;
}
</style>