<template>
    <div class="home center">
        <PageTitle icon="fa fa-home" main="Dashboard"
            sub=" Indra - Master of Knowledge" />
        <div class="stats">
            <Stat title="Categorias" :value="stat.categories"
                icon="fa fa-folder" color="#d54d50" />
            <Stat title="Artigos" :value="stat.articles"
                icon="fa fa-file" color="#3bc480" />
            <Stat title="Usuários" :value="stat.users"
                icon="fa fa-users" color="#3282cd" />       
        </div>    
    
<br>
<br>
        
        <PageTitle icon="fa fa-sticky-note" main="Site"
            sub="Para busca de informações" />

<br>
<br>
    <div class="home center">
        <b-card>
            <b-card  bg-variant="dark" text-variant="warning" title="">
                <p class="card-text">
                    <center>Aqui você pode encontrar todas as atualizações do app 99...</center>
                </p>
                 <center><b-button href="https://99app.com/motorista/" variant="warning">Entrar</b-button></center>
            </b-card>
        </b-card> 
    </div>
    </div>
</template>




<script>
import PageTitle from '../template/PageTitle'
import Stat from './Stat'
import axios from 'axios'
import { baseApiUrl } from '@/global'

export default {
    name: 'Home',
    components: { PageTitle, Stat },
    data: function() {
        return {
            stat: {}
        }
    },
    methods: {
        getStats() {
            axios.get(`${baseApiUrl}/stats`).then(res => this.stat = res.data)
        }
    },
    mounted() {
        this.getStats()
    }
}
</script>

<style>
    .stats {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }


.card {
  box-shadow: 0 60px 50px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 100%;
}




</style>


