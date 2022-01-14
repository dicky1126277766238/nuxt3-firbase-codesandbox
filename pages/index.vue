<script setup lang="ts">
  const firestore = await useFetch("/api/firestore");
  const {collections} = firestore.data.value;

  const auth = await useFetch("/api/auth");
  const {users} = auth.data.value;
</script>

<template>
  <div>
    <div>
      collections {{ collections }}
    </div>
    <div>
      users {{ users }}
    </div>
  </div>
</template>
