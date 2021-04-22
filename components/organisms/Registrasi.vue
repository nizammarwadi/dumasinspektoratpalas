<template>
    <section id="registrasi" class="registrasi">
        <div class="container">
            <div class="registration-content">
                <div class="col-md-4">
                    <h2 class="title">Form Pengaduan</h2>
                    <form>
                        <div class="form-group">
                            <label class="title-name" for="name">Nama</label>
                            <input v-model="name" @keypress="checkValue('name')" type="text" class="form-control" id="name" placeholder="Contoh: Ucok Bala Harahap">
                            <small id="error-name" class="form-text text-muted" style="color: red !important" v-if="errorName">{{ errorName }}</small>

                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input v-model="email" @keypress="checkValue('email')" type="email" class="form-control" id="email" placeholder="Contoh: ucokbala@mail.com">
                            <small id="error-email" class="form-text text-muted" style="color: red !important" v-if="errorEmail">{{errorEmail}}</small>

                        </div>
                        <div class="form-group">    
                            <label for="phone">Ponsel (Whatsapp)</label>
                            <input v-model="phone" @keypress="checkValue('phone')" type="number" class="form-control" id="phone" placeholder="Contoh: 0822 2123 5445">
                            <small id="error-phone" class="form-text text-muted" style="color: red !important" v-if="errorPhone">{{errorPhone}}</small>

                        </div>
                        <div class="form-group">
                            <label for="titleLaporan">Judul Laporan</label>
                            <input v-model="titleLaporan" @keypress="checkValue('titleLaporan')" type="text" class="form-control" id="title-laporan" placeholder="Contoh: Dana desa">
                            <small id="error-laporan" class="form-text text-muted" style="color: red !important" v-if="errorTitleLaporan">{{errorTitleLaporan}}</small>
                        </div>
                        <div class="form-group">
                            <label for="project">Jenis Laporan</label>
                            <input v-model="project" @keypress="checkValue('project')" type="text" class="form-control" id="project" placeholder="Contoh: Penyalahgunaan dana desa">
                            <small id="error-project" class="form-text text-muted" style="color: red !important" v-if="errorProject">{{errorProject}}</small>
                        </div>
                        <div class="form-group">
                            <label for="message">Isi Laporan</label>
                            <textarea v-model="message" @keypress="checkValue('message')" name="message" rows="5" id="message" class="form-control textarea" placeholder="Contoh: Silahkan tuliskan laporan anda secara jelas"></textarea>
                            <small id="error-message" class="form-text text-muted" style="color: red !important" v-if="errorMessage">{{errorMessage}}</small>

                        </div>
                        <div class="form-group">
                            <p class="message-file">Lampirkan file <span style="color:red; font-size:12px;">*jika ada*</span></p>
                            <input type="file" ref="fileUpload" class="form-control" id="project" placeholder="Contoh: Penyalahgunaan dana desa">
                        </div>
                        <div class="form-group flex-auto send-button">
                            <Button
                                data-toggle = 'modal'
                                data-target = '#exampleModal'
                                titleButton = 'Submit'
                                @click-button = 'clickRegister'
                            />
                        </div>
                        <div v-if= "sendData">
                           <Modal
                                @click-reset = 'clickClose'
                           />
                        </div>
                    </form>
                </div>
                <div class="col-md-6">
                    
                        <div class="card-body text-center registration-image">
                             <img  class="reg-image" src="~/assets/images/image-registration.svg"  alt="not found">
                        </div>
                </div>
            </div>
        </div>
           <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#007bff" fill-opacity="1" d="M0,32L48,58.7C96,85,192,139,288,160C384,181,480,171,576,186.7C672,203,768,245,864,224C960,203,1056,117,1152,101.3C1248,85,1344,139,1392,165.3L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
            </path></svg>
    </section>
</template>

<script>
import axios from 'axios'
import Button from "~/components/atoms/Button.vue"
import Modal from "~/components/mollecules/Modal.vue"
export default {
    components: {
        Button: Button,
        Modal: Modal,
    },
    data() {
        return {
            name: '',
            email: '',
            phone: '',
            titleLaporan: '',
            project: '',
            message: '',
            errorName: '',
            errorEmail: '',
            errorPhone: '',
            errorTitleLaporan: '',
            errorProject: '',
            errorMessage: '',
            errorFileUpload: '',
            sendData: false,
            sendFile: true,
        }
    },
    mounted() {
        
    },
    methods: {
        validataInput() {
            if (this.name == '') {
                this.errorName = 'Nama tidak boleh kosong'
            }
            if (this.email == '') {
                this.errorEmail = 'Email tidak boleh kosong'
            }
            if (this.phone == '') {
                this.errorPhone = 'No ponsel (WhatsApp) harus di isi'
            }
            if (this.titleLaporan == '') {
                this.errorTitleLaporan = 'Judul laporan harus di isi'
            }
            if (this.project == '' ) {
                this.errorProject = 'Jenis laporan harus di isi'
            }
            if (this.message == '') {
                this.errorMessage = 'Isi laporan harus di isi'
            }
            if (this.$refs.fileUpload) {
                if (this.$refs.fileUpload.files[0].size > 2 * 1024) {
                    this.errorMessage = 'File tidak boleh dari 2MB'
                    sendFile = false
                }
            }
        },
        clickRegister() {
            console.log(this.$refs.fileUpload)
            this.validataInput()
            if (this.name && 
                this.email &&
                this.phone && 
                this.titleLaporan && 
                this.project &&
                this.sendFile
                ) {
                    this.sendData = true

            }
        },
        checkValue(param) {
            if (param == 'name') {
                this.errorsName = ''
            }
            if (param == 'email') {
                this.errorEmail = ''
            }
            if (param == 'phone') {
                this.errorPhone = ''
            }
            if (param == 'title-laporan') {
                this.errorTitleLaporan = ''
            }
            if (param == 'project') {
                this.errorProject = ''
            }
            if (param == 'message') {
                this.errorMessage = ''
            }
        },
        clickClose() {
            this.name = ''
            this.email = ''
            this.phone = ''
            this.titleLaporan = ''
            this.project = ''
            this.message = ''
            this.fileUpload = ''
        },

    }
}
</script>

<style>
    /* .title-name {
        margin-left: -100;
    } */
    
    .message-file {
        margin-left: -170px;
    }
    .registration-content {
        display: flex;
        justify-content: space-around;
    }
    .registration-image {
        margin-top: 450px;
    }
    .title {
        font-size: 32px;
        font-weight: 700;
    }
    .form-control{
        font-size: 16px;
    }
    .textarea{
        padding: 5px px 5p 0px;
    }
    label{
        font-size: 18px;
        font-weight: 400;
    }
    .reg-image{
       width: 450px;
    }
    .color-svg {
        margin-top: -90px;
    }
    /* .row {
        align-items: center;
    } */
    .send-button Button {
        padding: 10px 30px;
        border-radius: 5px;
    }
    @media (max-width: 768px) {
        .registrasi {
            margin-top: 50px;
            padding: 0px 20px;
        }
        .card-body  {
            width: 100%;
            padding: 0px 0px;
            margin: 0px 0px;
        }
        .col-md-4 {
            width: 100%;
            padding: 0px 20px;
            margin: 0px 0px;
        }
        .col-me-6 {
            width: 100% !important;
            margin: 0px 0px;
            padding: 0px 0px;
        }
    }
    @media(max-width: 860px) {
         .reg-image{
            width: 100%;
            margin: 0px 0px;
            padding: 0px 0px;
        }
    }
</style>