<script setup>
import {computed} from 'vue';
import {siteConfig as c} from '../config/siteConfig';
const props=defineProps({course:{type:String,default:''},newClasses:Boolean});
const url=computed(()=>'https://wa.me/'+c.whatsapp.replace(/\D/g,'')+'?text='+encodeURIComponent(props.newClasses?'Olá! Vim pelo site e gostaria de informações sobre as novas turmas.':'Olá! Vim pelo site e gostaria de fazer minha matrícula'+(props.course?' no curso de '+props.course:'')+'.'));
</script>
<template><div class="enrollment-callout"><a class="primary enrollment-button" :href="url" target="_blank" rel="noopener noreferrer"><i class="mdi mdi-whatsapp" aria-hidden="true"/><span>{{newClasses?'Clique aqui para ter informações sobre as novas turmas':'Faça sua matrícula'}}</span><i class="mdi mdi-arrow-top-right" aria-hidden="true"/></a></div></template>
