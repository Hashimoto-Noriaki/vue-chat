<template>
    <div>
        <h2>ログイン</h2>
        <form>
            <input type="email" placeholder="メールアドレス" v-model="email">
            <input type="password" placeholder="パスワード" v-model="password">
            <div class="error">{{ error }}</div>
            <button>ログイン</button>
        </form>
        Eメール：{{ email }}
    </div>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            password: ''
        }
    }
}
</script>

