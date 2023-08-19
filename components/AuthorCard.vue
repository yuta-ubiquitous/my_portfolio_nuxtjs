<template>
  <div class="md:fixed">
    <div class="md:block flex justify-center items-center">
      <nuxt-img :src="siteMetadata.author_image" loading="lazy" alt="me"
        class="shadow-xl md:h-60 md:w-60 h-40 w-40 rounded-full" />
      <div class="mb-2 mx-7 mt-4 justify-center items-center">
        <h1 class="md:text-3xl text-2xl text-gray-800 font-bold dark:text-blue-100">
          {{ siteMetadata.author }}
        </h1>
        <div class="md:text-lg text-gray-600 dark:text-blue-100">
          {{ siteMetadata.position }}
        </div>
        <div class="md:text-base text-gray-500 dark:text-blue-100">
          最終更新日:
          <span
            class="bg-blue-100 text-blue-800 text-sm font-medium mr-2 px-2.5 py-0.5 rounded dark:bg-blue-200 dark:text-blue-800 ml-1">
            {{ siteMetadata.last_updated_at }}
          </span>
        </div>
      </div>
    </div>

    <div class="mx-7 hidden md:block">
      <div class="flex">
        <div class="my-1 mr-1 text-gray-600 dark:text-blue-100">
          <a :href="siteMetadata.twitter" target="_blank">
            <Twitter />
          </a>
        </div>
        <div class="my-1 text-gray-600 dark:text-blue-200">
          <a :href="siteMetadata.github" target="_blank">
            <Github />
          </a>
        </div>
        <div class="my-1 text-gray-600 dark:text-blue-200">
          <a :href="siteMetadata.note" target="_blank">
            <Note />
          </a>
        </div>
      </div>

      <div class="my-1 text-gray-600 dark:text-blue-200">
        <a :href="siteMetadata.qiita" target="_blank">
          <Qiita />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Twitter from "../assets/icon/icons8-twitter.svg?inline";
import Github from "../assets/icon/github_new.svg?inline";
import Note from "../assets/icon/note.svg?inline";
import Qiita from "../assets/icon/qiita.svg?inline";
import siteMetaInfo from "@/data/sitemetainfo";
export default {
  components: { Twitter, Github, Note, Qiita },
  data: () => {
    return {
      siteMetadata: siteMetaInfo,
    };
  },
};
</script>
