# testhtml
jimmyhelp

partie html :
<template>
  <div class="page-download">
    <Navbar />
    <!-- titre et sous titre -->
    <section class="text bg-download is-large is-light">
      <div id="pageTitle" class="container fullwidth disable-border">
      </div>

      <!-- partie windows -->
      <div id="windowsDownload" class="windows">
        <p class="windows has-text-centered mt-xlarge mt-akukamu has-text-light is-size-2">
          Downloads
        </p>
        <hr style="width: 20%; margin: auto; margin-top: 20px" />
        <div class="buttons is-centered mt-xlarge">
          <a class="button is-blacked">Windows 64 Bits <i class="fas fa-download" style="padding-left:5px; font-size:20px;"></i></a>
        </div>
        <div class="buttons is-centered mt-xxlarge mb-large">
          <a class="button is-blacked"> MAC OS <i class="fas fa-download" style="padding-left:5px; font-size:20px;"></i></a>
        </div>
        <div class="buttons is-centered mt-xxlarge mb-large">
          <a class="button is-blacked"> LINUX <i class="fas fa-download" style="padding-left:5px; font-size:20px;"></i></a>
        </div>
      </div>

      <!-- partie linux et mac -->
      <div id="linuxDownload" class="linux">
        <p class="linux has-text-centered mt-xlarge mt-akukamu has-text-light is-size-2">
          For Linux & Mac OS
        </p>
        <hr style="width: 20%; margin: auto; margin-top: 20px" />
        <div class="buttons is-centered mt-xlarge">
          <a class="button is-black mb-large"  v-on:click="redirectDownloadLinux">
            Linux & Mac OS Installation Page
          </a>
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
import Navbar from './Navbar';
import Footer from './Footer.vue';
export default {
  components: {
    Navbar,
    Footer    
    },
  name: "Download",
  props: {},
  methods : {
          redirectDownloadLinux() {      
             window.location = '/downloadLinux';
          }
      }
};
</script>

<style scoped>

.fullwidth {
  max-width: 100% !important;
}

.disable-border {
  border-radius: 0% !important;
}

</style>


PARTIE CSS :

.bg-download{
    background-image: url(pagedownload.png);
    
    background-size: cover;
}
