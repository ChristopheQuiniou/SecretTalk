<script>
    export default {
        props: [
            "modelValue"
        ],
        methods: {
            mettreAJour(){
                this.$emit("update:modelValue",{
                    auteur: this.$ref.auteur.value,
                    contenu: this.$ref.contenu.value
                })
            }
        },
        emits:[
            "update:modelValue"
        ]
    }
</script>
<template>
  <lable for="champAuteur">Auteur : </lable>
  <input :value="modelValue.auteur" ref="auteur" @input="mettreAJour()" id="champAuteur" type="text"><br>
  <label for="champContenu">Contenu : </label>
  <input id="champContenu" ref="contenu" type="text" min="3" max="254"><br>
  <button>Valider</button>
</template>