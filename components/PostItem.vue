<template>
  <div>
    <!-- Header post user -->
    <div class="bg-white shadow-md mb-3">
      <div class="w-100 border-solid border-2 border-gray-400 rounded-t-md flex justify-between p-5 pl-2 items-center">
        <div class="flex gap-5">
          <img src="https://via.placeholder.com/150" class="max-w-full rounded-full" width="52" height="52" alt="post placeholder"/>
          <div><p class="font-medium">Nama User</p></div>
        </div>
      </div>
    </div>
    <!-- Post Body -->
    <div>
      <img src="https://via.placeholder.com/584" class="min-w-full" width="584" height="470" alt="post placeholder"/>
    </div>
    <div class="px-3 py-2">
      <p><b>Adi</b></p>
      <p>ini deskripsi gambar</p>
    </div>
    <hr/>
    <div v-if="comments.length > 0">
      <CommentItem v-for="item in comments" :key="item.id" :message="item.message"/>
    </div>
    <div v-else>No Comment</div>
    <div class="flex p-2 gap-2 items-center w-full">
      <div>
        <img src="https://via.placeholder.com/150" class="max-w-full rounded-full" width="52" height="52" alt="post placeholder"/>
      </div>
      <div class="flex-1">
        <form action="">
          <input type="text" class="input-control w-full rounded-3xl" />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import CommentItem from './CommentItem.vue';
  export default {
    data() {
        return {
            comments: [
                {
                    id: 1,
                    message: "ini adalah komentarnya !"
                },
                {
                    id: 2,
                    message: "ini jugaaa adalah komentarnya !"
                },
                {
                    id: 3,
                    message: "ini jugaaa adalah komentarnya !"
                }
            ]
        };
    },
    components: { CommentItem }
}
</script>