<template>
    <div>
        <h1>HELLO {{ userName }}</h1>
        <p>{{ message }}</p>
    </div>
</template>

<script>
export default {
  data () {
    return {
      userName: 'Taehee',
      message: 'WELCOME🐰',
      arr: [],
      obj: {}
    }
  }
}
</script>

<!-- scoped: 이 화면에서만 -->
