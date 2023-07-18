<script setup>
    let menus = [
        {
          text: 'Home',
          link: '#home-section',
          children: [],
          active: true,
        },
        {
          text: 'Dropdown',
          link: '#',
          children: [
            {
              text: 'Testimonials',
              link: '#testimonials-section',
              children: [],
            },
            {
              text: 'Menu Two',
              link: '#',
              children: [
                {
                  text: 'Sub Menu One',
                  link: '#',
                  children: [],
                },
                {
                  text: 'Sub Menu Two',
                  link: '#',
                  children: [],
                },
                {
                  text: 'Sub Menu Three',
                  link: '#',
                  children: [],
                },
              ],
            },
            {
              text: 'Menu Three',
              link: '#',
              children: [],
            },
          ],
        },
        {
          text: 'Features',
          link: '#features-section',
          children: [],
        },
        {
          text: 'Pricing',
          link: '#pricing-section',
          children: [],
        },
        {
          text: 'About',
          link: '#about-section',
          children: [],
        },
        {
          text: 'Contact',
          link: '#contact-section',
          children: [],
        },
    ];
</script>

<template>
    <ul class="js-clone-nav d-none d-lg-inline-block site-menu float-left">
        <li v-for="menuItem in menus" :key="menuItem.text" :class="{ 'active': menuItem.active, 'has-children': menuItem.children.length > 0 }">
            <a :href="menuItem.link" class="nav-link">{{ menuItem.text }}</a>
            
            <ul v-if="menuItem.children.length > 0" class="dropdown">
              <li v-for="childItem in menuItem.children" :key="childItem.text" :class="{ 'active': childItem.active, 'has-children': childItem.children.length > 0 }">
                <a :href="childItem.link" class="nav-link">{{ childItem.text }}</a>

                <ul v-if="menuItem.children.length > 0" class="dropdown">
                    <li v-for="childItem in menuItem.children" :key="childItem.text">
                      <a :href="childItem.link" class="nav-link">{{ childItem.text }}</a>
                    </li>
                  </ul>
              </li>
            </ul>
        </li> 
    </ul>
</template>