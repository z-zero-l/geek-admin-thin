<script setup lang="ts">
import { Error } from '@/components/ErrorMessage'
import { usePermissionStore } from '@/store/modules/permission'
import { useRouter } from 'vue-router'

const { push } = useRouter()

const permissionStore = usePermissionStore()

const errorClick = () => {
  push(permissionStore.homePath as string)
}
</script>

<template>
  <Error @error-click="errorClick" />
</template>
