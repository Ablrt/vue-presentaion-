<template>
    <li v-if="student.isStudent">
        {{student.name + ' is in ' + student.dep}}
        <img src="https://pnggrid.com/wp-content/uploads/2021/12/Red-Among-us-PNG-Transparent.png" @click= "$emit('not-student', student.name)"/>
    </li>
    
</template>

<script>
export default({
    props:{
        student:{
            type:Object,
            required:true
        }
    }
})
</script>

<style scoped>
    li{
        border: 5xp  solid #ccc;
        display: flex;
        justify-content: space-between;
        padding: 0.5rem 2rem;
        margin-bottom: 1rem;
        width: 400px;
        font-size: 23px;
    }
    img{
       width: 30px;
    }
</style>
