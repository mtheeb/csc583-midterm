<template>
  <div class="column is-3">
    <aside class="menu">
      <ul class="menu-list">
        <li>
          <a @click="navigate('dashboard')">
            <span class="icon"><i class="fa fa-home"></i></span>
            <span>Home</span>
          </a>
        </li>
        <li>
          <a @click="navigate('users.list')">
            <span class="icon"><i class="fa fa-user"></i></span>
            <span>Users</span>
          </a>
        </li>
        <li>
          <a @click="navigate('items.list')">
            <span class="icon"><i class="fa fa-list"></i></span>
            <span>Items</span>
          </a>
        </li>
        <li>
          <a @click="logout">
            <span class="icon"><i class="fa fa-sign-out"></i></span>
            <span>Logout</span>
          </a>
        </li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  name: 'ccmenu',
  methods: {
    logout() {
      localStorage.clear();
      this.$router.push({ name: 'auth.signin' });
    },
    navigate(index) {
      this.$router.push({ name: index });
    },
  },
};
</script>
