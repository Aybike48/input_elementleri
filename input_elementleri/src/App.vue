<template>
    <div class="container">
        <form v-if!="göster">
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <label for="name">İsim</label>
                    <div class="mt-5">
                        <input class="form-group" placeholder="İsminizi Giriniz" type="text" v-model="userData.isim" >
                    </div>
                    <label for="name">email</label>
                    <div class="mt">
                        <input class="form-group" placeholder="Email Giriniz " type="email" v-model="userData.email" >
                    </div>
                    <label for="name">şifre</label>
                    <div class="mt">
                        <input class="form-group" placeholder="Şifre Giriniz" type="password" v-model="userData.sifre" >

                    </div>
                    <h3>Cinsiyet</h3>
                    <div class="mt">
                        <input class="form-group" type="radio" v-model="userData.cinsiyet" value="KADIN"> KADIN
                    </div>
                    <div class="mt">
                        <input class="form-group" type="radio" v-model="userData.cinsiyet" value="erkek"> erkek 
                    </div>   
                    <div class="mt">
                        <input class="form-group" type="radio" v-model="userData.cinsiyet" value="yok"> Belirtmek İstemiyorum
                    </div>                  
                    <button class="btn btn-primary" @click!="göster" @click.prevent="submit" >Gönder</button>
                </div>
            </div>
        </form>
        <hr>
        <div class="row" v-if="!göster">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-info">
                    <div class="panel-heading">
                        <h4>Girdiğiniz Bilgier</h4>
                    </div>
                    <div class="panel-body">
                        <p>Tam Ad:{{userData.isim}}</p>
                        <p>E-mail: {{userData.email}} </p>
                        <p>Şifre: {{userData.sifre}}</p>
                        <p>Cinsiyet: {{userData.cinsiyet}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
               userData : {                  
                    isim:" ",
                    email:" ",
                    sifre:" ",
                    cinsiyet:" "               
               },
               göster : false               
            };           
        }
    }
</script>

<style>
</style>
