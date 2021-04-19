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
                <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" @click="toProfilSection">PROFIL</a>
                </li>
                    <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" @click="toStrukturSection">TENTANG KAMI</a>
                </li>
                <!-- <li class="nav-item dropdown ">
                    <a class="nav-link dropdown-toggle text-white" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        PROGRAM
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" @click="toProgramSection">Visi dan Misi</a>
                    <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="#">RPJM DESA</a>
                    <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="#">RPJP DESA</a>
                    </div>
                </li> -->
                <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" href="#keuangan">HUBUNGI KAMI</a>
                </li>
                <!-- <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" href="#suratonline">SURAT ONLINE</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link js-scroll-trigger text-white" @click="toFooterSection">HUBUNGI KAMI</a>
                </li> -->
                <!-- <li class="nav-item">
                        <ButtonElement
                        titleBtn="LOGIN"
                    />
                </li> -->
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
            strukturSection: "",
            programSection: "",
            footer: "",
        }
    },
    mounted() {
        this.berandaSection = document.getElementById("slider")
        this.profilSection = document.getElementById("profil")
        this.strukturSection = document.getElementById("struktur")
        this.programSection = document.getElementById("program")
        this.footer = document.getElementById("footer")
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
        toStrukturSection() {
            this.strukturSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
        toProgramSection() {
            this.programSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest",
            })
            this.hideMenu()
        },
        toFooterSection() {
            this.footer.scrollIntoView({
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
    .navbar {
        background-color: rgb(104, 157, 213);
        /* background-color: yellow; */
        /* background-color: transparent; */
        font-weight: 650;
        padding: 0px 80px;
    }
    .navbar-nav {
        cursor: pointer;
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
       .navbar-nav {
           margin-right: 0px;
       }
       .palas {
           margin-left: 0px;
       }
    }
</style>
