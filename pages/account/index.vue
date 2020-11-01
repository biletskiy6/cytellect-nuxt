<template>
  <div class="account">
    <div class="container">
      <AccountInfo />
      <ChartTree />
    </div>
  </div>
</template>

<script>
import ChartTree from '@/components/ChartTree'
import AccountInfo from '@/components/AccountInfo'
export default {
  layout: 'auth',
  components: { AccountInfo, ChartTree }
}
</script>
