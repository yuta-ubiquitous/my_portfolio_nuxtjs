<template>
  <div class="mb-6">
    <h2 class="mt-6 text-3xl text-gray-700 font-bold capitalize dark:text-blue-200">
      その他
    </h2>
    <ul class="list-disc mt-4 ml-5">
      <li v-for="achevement in achevementData" class="pb-3">
        <p class="text-base font-bold">{{ achevement.name }}（{{ achevement.date }}）</p>
        <template v-for="(link, index) in achevement.links">
          <template v-if="index != 0">
            <p class="text-sm link-separetor">|</p>
          </template>
          <a :href="link.url" target="_blank" class="text-sm text-blue-800">
            {{ link.title }}
          </a>
        </template>
      </li>
    </ul>
  </div>
</template>

<script>
import achevements from "@/data/achevements";

// achevementsデータのソート処理
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

const sortedAchevements = sortByDateAndNameDescending(achevements);

export default {
  data: () => {
    return {
      achevementData: sortedAchevements,
    }
  }
};
</script>

<style>
.link-separetor {
  display:inline;
}
</style>
