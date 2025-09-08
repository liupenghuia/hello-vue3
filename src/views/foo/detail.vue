<template>
  <div class="detail">
    <h2>Detail Page</h2>
    <div class="actions">
      <button type="button" @click="goBack">
        <span>返回上一页</span>
      </button>
      <button type="button" @click="goBar">
        <span>跳转到 Bar</span>
      </button>
    </div>
  </div>
  
</template>

<script setup lang="ts">
const router = useRouter()

function goBack() {
  router.back()
}

function goBar() {
  router.push({ name: 'bar' })
}
</script>

<style lang="less" scoped>
.detail {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
}
.actions {
  display: flex;
  gap: 12px;
}
</style>


