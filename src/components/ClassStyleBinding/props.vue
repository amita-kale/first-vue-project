<template>
    <h1>{{name}}</h1>
</template>
<script>
import { propsToAttrMap } from '@vue/shared';

export default {
    name:propsToAttrMap,
    props:['name']
}
</script>