<template>
<div>
    <div class="nav">
        <div class="logo">
            <a href="#">Hallow<span>ee</span>nd</a>
            <img src="@/assets/logoimg.png" alt="Logo">
        </div>
        <div class="menu">
            <a href="#" @click.prevent="scrollTo('section1')">Home</a>
            <a href="#" @click.prevent="scrollTo('section2')">Category</a>
            <a href="#" @click.prevent="scrollTo('section3')">About</a>
            <a href="#" @click.prevent="scrollTo('section4')">Trick or Treat</a>
            <button class="btn">Donate</button>
            <button class="btn2" @click="openSidebar"><i class="fa fa-bars" aria-hidden="true"></i></button>
        </div>
    </div>
    <div class="side-bar" :class="{ active: isSidebarActive }">
        <div class="close-btn" @click="closeSidebar">
            <i class="fas fa-times"></i>
        </div>
        <div class="menu">
            <div class="item"><a href="#" @click.prevent="scrollTo('section1')"><i class="fa fa-home" aria-hidden="true"></i> Home </a></div>
            <div class="item"><a href="#" @click.prevent="scrollTo('section2')"><i class="fa fa-sitemap" aria-hidden="true"></i> Category </a></div>
            <div class="item"><a href="#" @click.prevent="scrollTo('section3')"><i class="fas fa-info-circle"></i> About </a></div>
            <div class="item"><a href="#" @click.prevent="scrollTo('section4')"><i class="fa fa-ticket" aria-hidden="true"></i> Trick or Treat </a></div>
        </div>
    </div>
</div>
</template>

  
<script>
export default {
    name: 'Header',
    data() {
        return {
            isSidebarActive: false
        };
    },
    methods: {
        openSidebar() {
            this.isSidebarActive = true;
        },
        closeSidebar() {
            this.isSidebarActive = false;
        },
        scrollTo(sectionId) {
            const element = document.getElementById(sectionId);
            if (element) {
                element.scrollIntoView({
                    behavior: 'smooth'
                });
            }
        }
    }
}
</script>
