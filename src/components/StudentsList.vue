<template>
    <div>  
        <ul>
            <StudentItem
            v-for="student of students" :key="student.id"
            v-bind:student="student"
            @not-student.="remove"/>
        </ul>
    </div>

</template>

<script>
import StudentItem from './StudentItem.vue'
export default {
    props:['students'],
    components:{
        StudentItem
    },
    methods:{
        remove(name){
            this.$emit('not-student', name);
        }
    }
}
</script>

<style scoped>
</style>
