<template>
    <div>
        <p v-if="error.length">           
            <b>Please correct the following error</b>
            <ul>
                <li v-for="e in error" v-bind:key="e.id">
                    {{e}}
                </li>
            </ul>           
        </p>
        <form @submit="login">
            <input type="text" v-model="name" name="name" placeholder="enter name"/><br><br>
            <input type="password" v-model="password" name="password" placeholder="enter password"/><br><br>
            <button type="submit">Login</button>
        </form>
    </div>
</template>

<script>
export default {
    name:'login',
    methods:{
        login(e)
        {   
            this.error=[];
            if(this.name && this.password)   
            {
                console.warn("no error");
                //return true
            }

            if(!this.name)
            {
                this.error.push("Username is required");
            }

            if(!this.password)
            {
                this.error.push("Password is required");
            }
            console.warn("Hello");
            e.preventDefault();        
        }
    },
    data(){
        return {
                error:[],
                name:null,
                password:null
        }
    }
}
</script>