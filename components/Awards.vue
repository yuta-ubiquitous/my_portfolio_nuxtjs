<template>
  <div class="mb-6">
    <h2 class="mt-6 text-3xl text-gray-700 font-bold capitalize dark:text-blue-200">
      受賞
    </h2>
    <ol class="list-decimal mt-4 ml-5">
      <li v-for="award in awardData" class="pb-3">
        <p class="text-base font-bold">{{ award.name }}（{{ award.date }}）</p>
        <template v-for="(link, index) in award.links">
          <template v-if="index != 0">
            <p class="text-sm link-separetor">|</p>
          </template>
          <a :href="link.url" target="_blank" class="text-sm text-blue-800">
            {{ link.title }}
          </a>
        </template>
      </li>
    </ol>
  </div>
</template>

<script>
import awards from "@/data/awards";

// awardsデータのソート処理
function sortByDateAndNameDescending(data) {
  return [...data].sort((a, b) => {
    // dateが降順となるようソート
    if (a.date > b.date) {
      return -1;
    } else if (a.date < b.date) {
      return 1;
    }

    // dateが同じ場合はnameが降順となるようソート
    if (a.name > b.name) {
      return -1;
    } else if (a.name < b.name) {
      return 1;
    }

    return 0;
  });
}

const sortedAwards = sortByDateAndNameDescending(awards);

export default {
  data: () => {
    return {
      awardData: sortedAwards,
    }
  }
};
</script>

<style>
.link-separetor {
  display:inline;
}
</style>
