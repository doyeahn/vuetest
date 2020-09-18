<template>
    <ul>
        <li v-for="s in subs" :class="s.type" :key="s.name">
            {{s.name}}
            <tree :subs="s.subs"></tree>
        </li>
    </ul>


</template>
<script type="text/javascript">
export default{
    name:'tree',
    props:['subs']
}
</script>