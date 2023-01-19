<script>
import axios from 'axios';
import AppCard from './AppCard.vue';

export default {
    name: "AppMain",
    components:{
        AppCard
    },
    data(){
    return{
      projects:[],
    }
  },
  created(){
    this.getProjects();
  },
  methods:{
    getProjects(){
      axios.get('http://127.0.0.1:8000/api/projects').then(resp => {
        this.projects = resp.data.results;
      })
    },
  }
}
</script>

<template>
    <div class="container">
        <h2 class="text-center">I Progetti</h2>
        <div class="row justify-content-center">
            <div class="col-9">
                <AppCard v-for="project in projects" :key="project.id"  :project="project"/>
            </div>
        </div>
    </div>
</template>

