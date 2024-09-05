<template>
    <div>
        これはコンポーネントから表示されています。
        <p>{{ message }}</p>
        <p>{{ isEnabled }}</p>
    </div>
</template>

<script>
export default {
    props:["message","isEnabled"]
}
</script>

