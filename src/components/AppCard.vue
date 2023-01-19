<script>
export default {
    name:"AppCard",
    data(){
        return{
            contentMaxLength: 50,
        }
    },
    props:{
        project: Object,
    },
    methods: {
        contentPreview(text) {
            if (text && text.length > this.contentMaxLength) {
                return text.substr(0, this.contentMaxLength) + '...';
            }
            return text;
        }
    }
}
</script>

<template>
<div class="card mb-3" >
    <div class="card-body mb-3 text-center">
        <h5 class="card-title">{{project.title}}</h5>
        <h6 class="card-subtitle mb-2 text-muted">{{project.slug}}</h6>
        <p class="card-text">{{contentPreview(project.content)}}</p>
        <a class="btn btn-primary" href="">Leggi di più</a>
    </div>
</div>
</template>