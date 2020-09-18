<template>
    <div>
        <h1>abc</h1>
        <h3>{{(new Date()).toTimeString()}}
        </h3>
        <h4> 조직도</h4>
        <tree :subs="contents" ></tree>
    </div>


</template>

<script type="text/javascript">
import tree from './Tree.vue';

export default{
    name:'contents',
    components:{tree},
    data: function()
    {
        return {
            contents:[
                {
                    name:"RMCF", type:"company",
                    subs: [
                        {name: "SI 사업부", type:"division",
                            subs: [
                                {name: "SI 1팀", type: "team"},
                                {name:"SI 2팀", type:"team"}
                            ]},
                    {name:"BI 사업부", type: "division",
                    subs : [
                        {name: "bi-1", type:"team"},
                        {name: "bi-2", type:"team"}
                    ]}
                    ]
                }
            ]
        }
    }
}
</script>