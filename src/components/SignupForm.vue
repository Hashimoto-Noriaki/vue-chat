<template>
    <div>
        <h2>アカウント登録</h2>
    <form @submit.prevent="signUp">
        <input type="text" required placeholder="名前" v-model="name">
        <input type="email" required placeholder="メールアドレス" v-model="email">
        <input type="password" required placeholder="パスワード" v-model="password">
        <input type="password" required placeholder="パスワード(確認用)" v-model="passwordConfirmation">
        <button>登録する</button>
    </form>
    </div>
</template>

<script>
export default {
    data(){
        return {
            name: "",
            email: "",
            password: "",
            passwordConfirmation: ''
        }
    },

    methods: {
        async signUp(){
            console.log(this.name, this.email, this.password, this.passwordConfirmation )
            // console.log(this.name, this.email, this.password, this.passwordConfirmation)
        }
    }
}
</script>
