<template>
  <div class="flex p-2 gap-2 items-center w-full">
    <div>
      <img src="https://via.placeholder.com/150" class="max-w-full rounded-full" width="52" height="52" alt="post placeholder"/>
    </div>
    <div class="flex-1">
      {{message}}
    </div>
  </div>
</template>
<script>
export default {
  props: {
    message: {
      type: String,
      required: true
    },
  }
}
</script>