---
layout: page
title: tags
sidebar: false
---

<Tags/>

<!-- <script setup>
import { ref, unref, computed, onMounted } from 'vue'
import  { data }  from '../.vitepress/theme/data/post.data'

const { tagMap,postMap } = data
const tags = Object.keys(tagMap)
const computedTagMap = computed(()=> {
  let result = {}
  for(let key in tagMap) {
    result[key] = tagMap[key].map(url => postMap[url])
  }
  return result
})

const currentTag = ref(null)
function onTagClick(newTag){
    currentTag.value = newTag
}
const postList = computed(()=> (unref(computedTagMap)[unref(currentTag)]))
onMounted(()=>{
  const searchParams = new URLSearchParams(window.location.search)
  if(searchParams.get('tag')) currentTag.value = searchParams.get('tag')
})

</script>
<div class="max-w-screen-lg w-full px-6 py-8 my-0 mx-auto">
    <div class="flex flex-wrap gap-4">
        <div v-for="(tag,i) in tags" :key="i" class="block py-1 px-4 bg-[var(--vp-c-bg-alt)] text-[var(--vp-c-text-1)] cursor-pointer hover:text-[var(--vp-c-brand)]" @click="onTagClick(tag)">
            <span>{{ tag }}</span>
            <span class="pl-1 text-[var(--vp-c-brand)]"> {{ computedTagMap[tag].length }}</span>
        </div>
    </div>
    <p v-text="currentTag" class="py-4 text-2xl"></p>
    <div v-for="(article, index) in postList" :key="index" class="flex justify-between items-center py-1 pl-6">
      <a v-text="article.title" :href="article.url" class="post-dot overflow-hidden whitespace-nowrap text-ellipsis">
      </a>
      <div v-text="article.date.string" class="pl-4 font-serif whitespace-nowrap" >
      </div>
    </div>
</div> -->