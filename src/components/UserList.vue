<template>
    <div class="list">
        <li
        class="list-item"
        v-for="user in users"
        :key=user.id
        >
        {{user.name}}
        </li>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { useUsers } from '@/use/users'

export default defineComponent({
  async setup () {
    const { users } = await useUsers()
    return { users }
  }
})
</script>
