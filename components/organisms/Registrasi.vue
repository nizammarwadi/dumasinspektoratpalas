<template>
    <section id="registrasi" class="registrasi">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-4">
                    <h2 class="title">Form Lapor</h2>
                    <form>
                        <div class="form-group">
                            <label for="name">Nama </label>
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
                            <label for="project">Jenis Laporan</label>
                            <input v-model="project" @keypress="checkValue('project')" type="text" class="form-control" id="project" placeholder="Contoh: Penyalahgunaan dana desa">
                            <small id="error-project" class="form-text text-muted" style="color: red !important" v-if="errorProject">{{errorProject}}</small>

                        </div>
                        <div class="form-group">
                            <label for="message">Isi Laporan</label>
                            <textarea v-model="message" @keypress="checkValue('message')" name="message" rows="5" id="message" class="form-control textarea" placeholder="Contoh: Silahkan tuliskan laporan anda secara jelas dan apabila ada lampiran yang perlu di cantumkan silahkan kirim ke Email kami inspektoratapalas@gmail.com"></textarea>
                            <small id="error-message" class="form-text text-muted" style="color: red !important" v-if="errorMessage">{{errorMessage}}</small>

                        </div>
                        <div class="form-group flex-auto send-button">
                            <Button
                                data-toggle = 'modal'
                                data-target = '#exampleModal'
                                titleButton = 'Daftar'
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
                    
                        <div class="card-body text-center">
                             <img  class="reg-image" src="~/assets/images/registration.png"  alt="not found">
                        </div>
                </div>
            </div>
        </div>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#0099ff" 
            fill-opacity="1" d="M0,32L48,53.3C96,75,192,117,288,138.7C384,160,480,160,576,176C672,192,768,224,864,202.7C960,181,1056,107,1152,96C1248,85,1344,139,1392,165.3L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
            </path></svg>
    </section>
</template>

<script>
import axios from 'axios'
import Button from "~/components/atoms/Button.vue"
// import Modal from "~/components/mollecules/Modal.vue"
export default {
    components: {
        Button: Button,
        // Modal: Modal,
    },
    data() {
        return {
            sendData: false,
            name: '',
            email: '',
            phone: '',
            project: '',
            message: '',
            errorName: '',
            errorEmail: '',
            errorPhone: '',
            errorProject: '',
            errorMessage: '',
        }
    },
    mounted() {
        
    },
    methods: {
        clickRegister() {
            this.validataInput()
            let payload = {
                fullname:this.name,
                email: this.email,
                whatsapp: this.phone,
                project_title: this.project,
                project_description: this.message
            }
            axios.post('https://bimbinganbareng-api.herokuapp.com/',payload)
            .then(res=>{
                console.log('kalau berhasil');
                console.log(res);
                this.sendData = true    
            })
            .catch(err=>{
                console.log('kalau error');
                console.log(err);
            })
        },
        validataInput() {
            if (this.name == '') {
                this.errorName = 'Nama tidak boleh kosong'
            }
            if (this.email == '') {
                this.errorEmail = 'Email tidak boleh kosong'
            }
            if (this.phone == '') {
                this.errorPhone = 'Wajib di isi'
            }
            if (this.project == '' ) {
                this.errorProject = 'Wajib di isi'
            }
            if (this.message == '') {
                this.errorMessage = 'Wajib di isi'
            }
        },
        checkValue(param) {
            if (param == 'name') {
                this.errorName = ''
            }
            if (param == 'email') {
                this.errorEmail = ''
            }
            if (param == 'phone') {
                this.errorPhone = ''
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
            this.project = ''
            this.message = ''
        }
    }
}
</script>

<style>
    .registrasi {
        padding: 80px;
    }
    .title {
        font-size: 32px;
        font-weight: 700;
        margin-bottom: 25px;
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
    .row {
        align-items: center;
    }
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