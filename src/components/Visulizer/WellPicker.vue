<template>
    <div id="list-group-items">
        <label class="list-group-item list-group-item-action" role="tab">
            <a class="title">{{title}}</a>
            <input 
            v-on:click="$emit('well-select', title)"
            class="chkBox" 
            type="checkbox">
        </label>
    </div>
</template>

<script>
export default {
    name: 'WellPicker',
    props: ['title']
}
</script>

<style>
</style>
