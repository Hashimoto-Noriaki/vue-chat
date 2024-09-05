<template>
    <div>
        これはコンポーネントから表示されています。
        <p>{{ message }}</p>
    </div>
</template>

<script>
export default {
    props:["message"]
}
</script>

