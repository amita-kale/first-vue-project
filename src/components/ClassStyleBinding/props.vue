<template>
    <!-- <h1>{{name}}</h1> -->
    <h3 v-for="user in users" :key="user.name">{{user.name}}</h3>
</template>
<script>
import { propsToAttrMap } from '@vue/shared';

export default {
    name:propsToAttrMap,
    props:['users']
}
</script>