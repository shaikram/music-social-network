<script setup>
import RouterLinkButton from '../../global/RouterLinkButton.vue'

</script>

<template>
  <div>
    <div class="mx-auto py-4">
      <div class="flex flex-wrap font-bold text-gray-100">
        <div class="text-gray-900 text-xl">Post</div>
        <div class="bg-green-500 w-full h-1"></div>

        <div class="w-full mt-4">
          <RouterLinkButton btnText="Create Post" color="green" url="/account/create-post" />
        </div>
      </div>
    </div>

    <div class="flex flex-wrap mb-4">
      <div class="my-1 px-1 w-full md:w-1/2 lg:w-1/2">
        <div class=" rounded-lg border">
          <a href="#">
            <img class="rounded-t-lg" src="https://via.placeholder.com/500x300" alt="" />
          </a>
          <div class="p-2 md:p-4">
            <div class="text-lg">
              <router-link 
                    to="" 
                    class="
                          underline 
                          text-blue-500
                          hover:text-blue-600
                          "
                >
                Test Title
              </router-link>
            </div>
            <p class="py-2">Location: Test Location</p>
            <p class="text-gray-darker text-md">
              It is a long established fact that a reader will be distracted
              by the readable content of a page when looking at its layout. 
              The point of using Lorem Ipsum is that it has a more-or-less normal 
              distribution of letters, as opposed to using 'Content here, content 
              here', making it look like readable English. Many desktop publishing 
              packages and web page editors now use Lorem Ipsum as their default 
              model text, and a search for 'lorem ipsum' will uncover many web 
              sites still in their infancy. Various versions have evolved over 
              the years, sometimes by accident, sometimes on purpose (injected humour and the like).
            </p>
            <div class="mt-2 flex items-center justify-end">
              <router-link 
                    to="/account/edit-post" 
                    class="
                          bg-blue-500
                          hover:bg-blue-700
                          text-white
                          text-sm
                          font-bold
                          py-1
                          px-2
                          rounded-full
                          "
                >
                Edit Post
              </router-link>
              <button
                    to="" 
                    class="
                          bg-red-500
                          hover:bg-red-700
                          text-white
                          text-sm
                          font-bold
                          py-1
                          px-2
                          rounded-full
                          "
                >
                Delete Post
              </button>
            </div>
        
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
>
