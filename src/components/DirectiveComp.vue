<template>
    <div>
       <h2>Filter Example</h2>
       {{10 | double}}
       {{'M' | gender | capitalize}}
        
    </div>
</template>

<script>
export default {
    name: 'DirectiveComp',
     data() {
            return {
                message :"Hello"
            }
        },
    filters:{
        capitalize(value){
            return value.toUpperCase();
        }
        ,
        double : function(value){
            return value * 2
        },
        gender : function(value){
            let data = value.toUpperCase();
            if(data == 'M'){
                return "Male"
            }else if(data == 'F'){
                return "Female"
            }
            return 'Not a Known Value'
        }
    },
    directives:{
        fontSizeargs : {
            inserted: function(el, binding){
                el.style.fontSize = binding.value+'px';
            }
        },
        changingStyle: {
                inserted : function(el){
                    el.style.color = "blue";
                    el.style.backgroundColor = "pink"
                }
        },
        demo: {
            inserted: function (el, binding, vnode) {
            var s = JSON.stringify
            el.innerHTML =
                'name: '       + s(binding.name) + '<br>' +
                'value: '      + s(binding.value) + '<br>' +
                'expression: ' + s(binding.expression) + '<br>' +
                'argument: '   + s(binding.arg) + '<br>' +
                'modifiers: '  + s(binding.modifiers.a) + '<br>' +
                'vnode keys: ' + Object.keys(vnode).join(', ')
            }
        },
           
    }
    
    
   
}
</script>

<style>

</style>
