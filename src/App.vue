<template>
  <NavBar
    :pages="pages"
    :active-page="activePage"
    :nav-link-click="(index) => (activePage = index)"
  />
  <p>Hello vue</p>
  <PageViewer :page="pages[activePage]" />
</template>

<script>
import PageViewer from "./components/PageViewer.vue";
import NavBar from "./components/NavBar.vue";

export default {
  components: {
    PageViewer,
    NavBar,
  },
  data() {
    return {
      activePage: 0,
      pages: [
        {
          link: { text: "Home", url: "index.html" },
          pageTitle: "Home Page",
          content: "This is home page content",
        },
        {
          link: { text: "About", url: "about.html" },
          pageTitle: "About Page",
          content: "This is About page content",
        },
        {
          link: { text: "Contact", url: "Contact.html" },
          pageTitle: "Contact Page",
          content: "This is Contact page content",
        },
      ],
    };
  },
};
</script>
