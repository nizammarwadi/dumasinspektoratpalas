<template>
    <section id="registrasi" class="registrasi">
        <div class="container">
            <div class="registration-content">
                <div class="form-reg">
                    <h2 class="title">FORM PENGADUAN</h2>
                    <form>
                        <div class="form-group">
                            <label class="title-name" for="name">Nama</label>
                            <input v-model="name" @keypress="checkValue('name')" type="text" class="form-control" id="name" placeholder="Contoh: Ucok">
                            <small id="error-name" class="form-text text-muted" style="color: red !important" v-if="errorName">{{ errorName }}</small>

                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input v-model="email" @keypress="checkValue('email')" type="email" class="form-control" id="email" placeholder="Contoh: ucok@gmail.com">
                            <small id="error-email" class="form-text text-muted" style="color: red !important" v-if="errorEmail">{{errorEmail}}</small>

                        </div>
                        <div class="form-group">    
                            <label for="phone">Ponsel (Whatsapp)</label>
                            <input v-model="phone" @keypress="checkValue('phone')" type="number" class="form-control" id="phone" placeholder="Contoh: 082221235445">
                            <small id="error-phone" class="form-text text-muted" style="color: red !important" v-if="errorPhone">{{errorPhone}}</small>

                        </div>
                        <div class="form-group">
                            <label for="titleLaporan">Judul Laporan</label>
                            <input v-model="titleLaporan" @keypress="checkValue('titleLaporan')" type="text" class="form-control" id="title-laporan" placeholder="Contoh: Dana desa">
                            <small id="error-laporan" class="form-text text-muted" style="color: red !important" v-if="errorTitleLaporan">{{errorTitleLaporan}}</small>
                        </div>
                        <div class="form-group">
                            <label for="subjectLaporan">Subjek Laporan</label>
                            <input v-model="subjectLaporan" @keypress="checkValue('subjectLaporan')" type="text" class="form-control" id="subjectLaporan" placeholder="Contoh: Kepala desa">
                            <small id="error-subjectLaporan" class="form-text text-muted" style="color: red !important" v-if="errorSubjectLaporan">{{errorSubjectLaporan}}</small>
                        </div>
                        <div class="form-group">
                            <label for="isiLaporan">Isi Laporan</label>
                            <textarea v-model="isiLaporan" @keypress="checkValue('isiLaporan')" name="isiLaporan" rows="5" id="isiLaporan" class="form-control textarea" placeholder="Contoh: Silahkan tuliskan laporan anda secara jelas"></textarea>
                            <small id="error-isiLaporan" class="form-text text-muted" style="color: red !important" v-if="errorIsiLaporan">{{errorIsiLaporan}}</small>

                        </div>
                        <div class="form-group">
                            <label for="file-upload">Lampirkan File Pendukung <span style="color: red; font-size: 12px;">*termasuk KTP anda & bukti lainnya dalam 1 file*</span></label>
                            <!-- <p class="isiLaporan-file">Lampirkan file <span style="color:red; font-size:12px;">*jika ada*</span></p> -->
                            <input @change="previewFiles" type="file" ref="fileUpload" class="form-control" id="subjectLaporan" placeholder="">
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
                <div class="image-form">
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
            subjectLaporan: '',
            isiLaporan: '',
            errorName: '',
            errorEmail: '',
            errorPhone: '',
            errorTitleLaporan: '',
            errorSubjectLaporan: '',
            errorIsiLaporan: '',
            errorFileUpload: '',
            file: null,
            sendData: false,
            sendFile: true,
        }
    },
    mounted() {
        
    },
    methods: {
        previewFiles(event) {
            this.file = event.target.files
        },
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
            if (this.subjectLaporan == '' ) {
                this.errorSubjectLaporan = 'Subjek laporan harus di isi'
            }
            if (this.isiLaporan == '') {
                this.errorIsiLaporan = 'Isi laporan harus di isi'
            }
           
            // if (this.$refs.fileUpload) {
            //     if (this.$refs.fileUpload.files[0].size > 2 * 1024) {
            //         this.errorisiLaporan = 'File tidak boleh dari 2MB'
            //         sendFile = false
            //     }
            // }
        },
        clickRegister() {
            this.validataInput()
            if (this.name && 
                this.email &&
                this.phone && 
                this.titleLaporan && 
                this.subjectLaporan &&
                this.sendFile) {
                    const formData = new FormData()
                    formData.append('nama', this.name)
                    formData.append('email', this.email)
                    formData.append('no_hp', `'${this.phone}`)
                    formData.append('judul_laporan', this.titleLaporan)
                    formData.append('subjek_laporan', this.subjectLaporan)
                    formData.append('isi_laporan', this.isiLaporan)
                    formData.append('file', this.file[0])
                    axios.post('https://powerful-caverns-77607.herokuapp.com/', formData, {
                        headers: {'Content-Type': 'multipart/form-data'
                    }})
                    .then(res=>{
                        console.log('kalau berhasil');
                        console.log(res);
                        this.sendData = true    
                    })
                    .catch(err=>{
                        console.log('kalau error');
                        console.log(err);
                    })
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
            if (param == 'titleLaporan') {
                this.errorTitleLaporan = ''
            }
            if (param == 'subjectLaporan') {
                this.errorSubjectLaporan = ''
            }
            if (param == 'isiLaporan') {
                this.errorIsiLaporan = ''
            }
        },
        clickClose() {
            this.name = ''
            this.email = ''
            this.phone = ''
            this.titleLaporan = ''
            this.subjectLaporan = ''
            this.isiLaporan = ''
            this.fileUpload = ''
        },

    }
}
</script>

<style>
    /* .title-name {
        margin-left: -100;
    } */
    
    .isiLaporan-file {
        margin-left: -170px;
    }
    .registrasi {
        margin-top: 40px;
    }
    .registration-content {
        display: flex;
        justify-content: space-around;
        align-items: flex-start;
    }
    .registration-image {
        margin-top: 450px;
    }
    .title {
        font-size: 23px;
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
    @media(max-width: 1024px) {
        .image-form 
        .registration-image .reg-image {
            display: none;

        }
    }
    @media(max-width: 860px) {
        .image-form {
            display: none ;
        }
        .form-group {
            padding: 0px 5%;
        }
        .form-reg .title {
            text-align: center;
            margin: 70px 0px 30px 0px;
        }
      
    }
</style>