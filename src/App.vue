// html
<template>
  <div>
    <StudentsList
    v-bind:students="students"
    @not-student="correctRole"/>
  </div>
</template>

//js (optinal)
<script>
import StudentsList from './components/StudentsList.vue'

export default {
  name: 'App',
  data(){
    return {
      students:[{name:'Saro', dep:'CS', isStudent:true},
                {name:'Maro', dep:'BS', isStudent:true},
                {name:'Taro', dep:'EC', isStudent:true},
                {name:'Karo', dep:'DS', isStudent:true},
                {name:'Aro', dep:'Hufflepuff', isStudent:true},
                {name:'Maro 2', dep:'CS', isStudent:true}]
    }
  },
  methods:{
    correctRole(n){
      let a = this.students.find(s=>{
        return s.name === n
      }) 
    a.isStudent = false
    }
    
  },
  components: {
    StudentsList
  }
}
</script>

//css (optinal)
<style scoped>

</style>
