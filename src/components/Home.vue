<template>
<div>
    <Header />
    <Section1 id="section1" />
    <Section2 id="section2" />
    <Section3 id="section3" />
    <Section4 id="section4" />
    <Section5 id="section5" />
    <Footer />
</div>
</template>

<script>
import Header from './Header.vue';
import Section1 from './Section1.vue';
import Section2 from './Section2.vue';
import Section3 from './Section3.vue';
import Section4 from './Section4.vue';
import Section5 from './Section5.vue';
import Footer from './Footer.vue';

export default {
    name: 'Home',
    components: {
        Header,
        Section1,
        Section2,
        Section3,
        Section4,
        Section5,
        Footer
    }
}
</script>
