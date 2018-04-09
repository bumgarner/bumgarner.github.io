<template lang="html">
    <div>
        <mobile-header></mobile-header>
        <app-header></app-header>
        <div id="main">
            <app-sidebar></app-sidebar>
            <app-contents></app-contents>
        </div>
    </div>
</template>

<script>
import MobileHeader from '@/components/header/MobileHeader'
import AppHeader from '@/components/header/AppHeader'
import AppSidebar from '@/components/content/AppSidebar'
import AppContents from '@/components/content/AppContents'

export default {
    components:{
        AppHeader,
        MobileHeader,
        AppSidebar,
        AppContents
    },
    name: "Push"
    // data() {
    //     return
    // }
}
</script>

<style scoped>
@import "../css/common.css"; 
</style>

