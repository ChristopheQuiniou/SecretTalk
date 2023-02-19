<script>
import Message from "./components/Message.vue"
import FormulaireMessage from "./components/FormulaireMessage.vue"
export default {
    components:{
        Message,
        FormulaireMessage
    },
    data(){
        return {
            message : {contenu:"Mon message",auteur:"Mon nom"},
            messages: [
                {contenu:"Hey salut",auteur:"Michel"}
            ]
        }
    }
}
</script>

<template>
    <h1>Secret Talk</h1>
    <p>Bienvenue !</p>
    <p>Secret Talk est une application web vous permettant de communiquer avec des personnes du mon entier.</p>
    <hr>
    <p v-if="messages.length == 0">Il n'y a pas encore de message ! Allez-y en premier 😉 </p>
    <Message v-for="message in messages" :auteur="message.auteur" :contenu="message.contenu"/>
    <hr>
    Auteur dbg :{{ message.auteur }}
    <FormulaireMessage v-model="message"/>
</template>

