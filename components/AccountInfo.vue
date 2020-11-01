<template>
  <div class="account-info">
    <h2 class="account-info__header">Welcome Back, Vsebolod!</h2>
    <ul class="account-notifications">
      <li class="account-notifications__item">
        You have <span class="warning">20</span> new notifications
      </li>
      <li class="account-notifications__item">
        You have <span class="white">5</span> new tasks
      </li>
      <li class="account-notifications__item">
        You have <span class="white">50</span> new messages
      </li>
      <li class="account-notifications__item">
        You have <span class="danger">1</span> problem
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AccountInfo'
}
</script>

<style scoped></style>
