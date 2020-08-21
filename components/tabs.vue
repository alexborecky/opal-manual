<template>
    <div class="full-width flex column">
        <div class="tab-bar flex">
            <div 
                :class="{'active': currentTab == 1}" 
                class="tab flex " 
                @click="selectTab(1)">
                <p>{{tabOneTitle}}</p>
            </div>
            <div 
                :class="{'active': currentTab == 2}" 
                class="tab flex " 
                @click="selectTab(2)">
                <p>{{tabTwoTitle}}</p>
            </div>
            <div 
                :class="{'active': currentTab == 3}" 
                class="tab flex " 
                @click="selectTab(3)">
                <p>{{tabThreeTitle}}</p>
            </div>
        </div>

        <div class="tab-content">
            <div v-if="currentTab == 1" class="text">
                <slot name="tabOne"></slot>
            </div>

            <div v-if="currentTab == 2" class="text">
                <slot name="tabTwo"></slot>
            </div>

            <div v-if="currentTab == 3" class="text">
                <slot name="tabThree"></slot>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: 'tabs',
    data () {
        return {
            currentTab: 1,
            isActive: ''
        }
    },
    methods: {
        selectTab(selectedTab) {
            this.currentTab = selectedTab
        },
    },
    props: [
        'tabOneTitle',
        'tabTwoTitle',
        'tabThreeTitle'
    ]
}
</script>

<style lang="scss" scoped>

.text {
    width: 100%;
    min-height: 100px;
}

.tab-bar {
    .active {
        background-color: rgba($color: $blue-color, $alpha: .2);
        p {
            color: $blue-color;
            font-weight: 600;
        }
    }
    .tab {
        border-radius: 5px;
        width: calc(100%/3);
        margin: 0 16px 0 0;
        p {
            padding: 16px;
        }
        &:hover {
            cursor: pointer;
            background-color: rgba($color: $blue-color, $alpha: .2);
        }
    }
}

    
</style>