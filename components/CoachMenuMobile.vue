<template>
    <div v-if="menuState">
        <div class="menu">
            <ul>
                <li v-for="(listItem, listItemIndex) in menuList" :key="listItemIndex">
                    {{listItem.title}}
                </li>
            </ul>
            <div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'CoachMenuMobile',
  props: {
    value: {
      type: Boolean,
      default:false
    }
  },data(){
    return {
        menuList:[
            {
                title:'Програми тренувань',
                link:''
            },
            {
                title:'Дієтологія',
                link:''
            },
             {
                title:'Результати',
                link:''
            },
            {
                title:'Пробне заняття',
                link:''
            },
             {
                title:'Контакти',
                link:''
            }
        ]
        
        }
    },
    computed:{
       menuState: {
      get() {
        return this.value;
      },
      set(v) {
        this.$emit('input', v);
      },
    },
    }
  }
  
</script>
<style scoped>
.menu{
  margin-top:40px;
  border:1px solid red;
}
</style>
