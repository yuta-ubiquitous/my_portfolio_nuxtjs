<template>
  <div class="md:fixed">
    <div class="md:block flex justify-center items-center">
      <nuxt-img
        :src="siteMetadata.author_image"
        loading="lazy"
        alt="me"
        class="shadow-xl md:h-60 md:w-60 h-40 w-40 rounded-full"
      />
      <div class="mb-2 mx-7 mt-4 justify-center items-center">
        <h1
          class="md:text-3xl text-2xl text-gray-800 font-bold dark:text-blue-100"
        >
          {{ siteMetadata.author }}
        </h1>
        <div class="md:text-lg text-gray-600 dark:text-blue-100">
          {{ siteMetadata.position }}
        </div>
        <a
          :href="`mailto:${siteMetadata.email}`"
          class="text-gray-600 md:hidden mt-1 dark:text-blue-100"
        >
          {{ siteMetadata.email }}
        </a>
      </div>
    </div>

    <div class="mx-7 hidden md:block">
      <div class="my-2 text-gray-600 flex dark:text-blue-100">
        <Twitter />
        <a :href="siteMetadata.twitter"> {{ siteMetadata.twitter_user }}</a>
      </div>
      <div class="my-2 text-gray-600 flex dark:text-blue-200">
        <Github />
        <a :href="siteMetadata.github"> {{ siteMetadata.githubUser }}</a>
      </div>
      <div class="my-2 text-gray-600 flex dark:text-blue-200">
        <Note />
        <a :href="siteMetadata.note"> {{ siteMetadata.note_user }}</a>
      </div>
      <div class="my-2 text-gray-600 flex dark:text-blue-200">
        <Qiita />
        <a :href="siteMetadata.qiita"> {{ siteMetadata.qiita_user }}</a>
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
  components: { Twitter, Github, Note, Qiita},
  data: () => {
    return {
      siteMetadata: siteMetaInfo,
    };
  },
};
</script>
