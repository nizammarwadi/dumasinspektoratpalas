<template>
  <div>
      <nav id="navbar" class="navbar navbar-expand-lg navbar-dark fixed-top">
        <img class="navbar-brand palas" src="~/assets/images/padang-lawas.png" width="50px" height="60px">
        <div class="logo mr-auto">
            <label for="siundol" style="font-weight:bold">E-DUMAS INSPEKTORAT</label>
            <p>Kabupaten Padang Lawas</p>
        </div>
        <button class="navbar-toggler " type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto mr-5">
                <li class="nav-item active">
                    <a class="nav-link js-scroll-trigger" href="#">BERANDA <span class="sr-only">(current)</span></a>
                </li>
                <li class="nav-item dropdown ">
                    <a class="nav-link dropdown-toggle text-white" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        PROFIL
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" @click="toProfilSection">TENTANG KAMI </a>
                    <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="/struktur-inspektorat">STRUKTUR</a>
                    </div>
                </li>
                    <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" @click="toFlowusersSection">PROSES</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" href="/news">BERITA</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" @click="toFooterSection">HUBUNGI KAMI</a>
                </li>
            </ul>
        </div>
    </nav>
  </div>
</template>

<script>
// import Button from '~/components/atoms/Button.vue' 
export default {
    components: {
        // ButtonElement: Button,
    },
    data() {
        return {
            berandaSection: "",
            profilSection: "",
            flowusersSection: "",
            teamSection: "",
            footerSection: "",
        }
    },
    mounted() {
        this.berandaSection = document.getElementById("navbar")
        this.profilSection = document.getElementById("about")
        this.flowusersSection = document.getElementById("flowusers")
        this.teamSection = document.getElementById("team")
        this.footerSection = document.getElementById("footer")
    },
    methods: {
        hideMenu() {
            let menuContainer = document.getElementById("navbarNav")
            menuContainer.classList.remove("show")
        },
        toBerandaSection() {
            this.berandaSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
        toProfilSection() {
            this.profilSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
        toFlowusersSection() {
            this.flowusersSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
        toTeamSection() {
            this.teamSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
        toFooterSection() {
            this.footerSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
    }
}
</script>

<style>
    .dropdown-menu.show {
        background-color: #007bff;
        border: none;
        margin-left: 70px;
        border-bottom-right-radius: 25px;
        color: white !important;
    }
    a .dropdown-item:hover{
        background-color: black;
    }
    .navbar {
        /* background-color: rgb(104, 157, 213); */
        background-color: #007bff;
        /* background-color: yellow; */
        /* background-color: transparent; */
        font-weight: 650;
        padding: 0px 80px;
    }
    .navbar-nav {
        cursor: pointer;
        font-size: 15px;
    }
    .palas {
        object-fit: contain;
        margin-left: 35px;
    }
    .logo {
        color: #f8f9fa;
        display: block;
        margin-top: 13px;
        line-height: 10px;
    }
    @media (max-width: 768px) {
        .logo {
            font-size: 13px;
        }
       .navbar {
           margin-right: 0px;
           padding: 0px 20px;
       }
       .palas {
           margin-left: 0px;
       }
    }
     @media (max-width: 400px) {
         .navbar {
             padding: 0px 5px;
         }
     }
</style>
