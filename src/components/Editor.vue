<template>
  <div v-html="target" @input="update" contenteditable="true"> </div>
</template>

<script>
export default {
  name: 'Editor',
  props: {
    value: String
  },
   data: function () {
        return {
            code: this.value,
            mark: false,//值改变是否是在View中改变
        }
    },
   computed: {//计算属性，可以直接调用
        target: function () {
            return this.code;
        },
    },
    methods: {
        update:function(event){
            this.mark = true;
            this.$emit('input', this.$el.innerText);//view->model
        }
    },
    watch: {
        'value': function () {//model->view
         console.log(!this.mark)
            if (!this.mark) {//避免view->model->view, 导致光标定位问题
                this.$el.innerHTML = this.value;
            }
            this.mark = false;
        }
    }
}
</script>

<style scoped lang="scss">
 
</style>
