<template>
    <div class="flex flex-col">
        
        <!----- PreviewnCard Whats happening ----->
        
        
        <SidebarRightPreviewCardVue title="What's Happening">
            
            <SidebarRightPreviewCardVueItem v-for="whatshappening in whatshappeningItems">
                <div>
                    <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatshappening.title }}</h2>

                    <p class="text-xs text-gray-400">
                        {{ whatshappening.count }}
                    </p>
                </div>
            </SidebarRightPreviewCardVueItem>

        </SidebarRightPreviewCardVue>
        <!----- PreviewnCard Who to follow ----->

        <SidebarRightPreviewCardVue title="Who to follow">
            
            <SidebarRightPreviewCardVueItem v-for="whotToFollow in whotToFollowItems">
                <div class="flex flex-row items-center justify-between p-2">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full"  :src="whotToFollow.image" :alt="whotToFollow.name">

                        <div class="flex flex-col ml-2">
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whotToFollow.name }}</h1>
                            <p class="text-xs text-gray-400">{{ whotToFollow.handle }}</p>
                        </div>
                    </div>
                    <div class="flex h-full">
                        <button
                            class="px-4 py-2 text-xs font-bold text-white bg-black rounded-full dark:text-black dark:bg-white">Follow</button>
                    </div>
                </div>
            </SidebarRightPreviewCardVueItem>

        </SidebarRightPreviewCardVue>

        

        <div>

        </div>

    </div>
</template>

<script setup>
//import image from "~/assets/images/images.jpg"
    const whatshappeningItems = ref([
        {
            title: 'SpaceX',
            count: '18.8k Tweets'
        },
        {
            title: '#CodingIsFun',
            count: '8.8k Tweets'
        },
        {
            title: '#artForall',
            count: '1.8k Tweets'
        }
    ])

    const whotToFollowItems = ref([
        {
            name: 'Ali',
            handle: '@JoeBiden',
            image: 'https://picsum.photos/200/200'
        },
        {
            name: 'Raza',
            handle: '@WebDeveloper',
            image: 'data:image/jpeg;base64,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'

        }
    ])
</script>