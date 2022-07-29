<script lang="ts" setup>
const { signOut, isLoggedIn } = useAuth();
const router = useRouter();

const handleSignOut = () => {
  signOut();
  router.push("/");
};
</script>

<template>
  <nav>
    <ul>
      <li>
        <NuxtLink to="/">Home</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/myprofile">Profile</NuxtLink>
      </li>
      <li v-if="isLoggedIn()" class="logout" @click="handleSignOut">Logout</li>
    </ul>
  </nav>
</template>

<style scoped>
nav {
  background: black;
  height: 10vh;
}

ul {
  display: flex;
  height: 100%;
  align-items: center;
  padding: 0 2rem;
}

li {
  color: white;
  margin-right: 1rem;
}

.logout {
  margin-left: auto;
  cursor: pointer;
}
</style>
