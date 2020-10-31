<template>
  <div class="account">
    <AccountInfo />
    <ChartTree />
  </div>
</template>

<script>
import ChartTree from '~/components/ChartTree'
import AccountInfo from '~/components/AccountInfo'
export default {
  components: { AccountInfo, ChartTree }
}
</script>
