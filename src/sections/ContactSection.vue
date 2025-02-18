<template>
    <section id="contact-section" class="px-12 lg:px-32 py-16 relative w-full min-h-screen flex justify-center items-center">
        <div class="w-full max-w-2xl bg-[#2a214c] shadow-lg p-8 rounded-lg text-white"  id="contact">

            <h1 class="uppercase text-4xl mb-6 font-semibold text-center text-[#fbbc35]">
                Contactez-nous
            </h1>

            <form @submit.prevent="submitForm" class="flex flex-col space-y-4">
                <label for="user_civilite" class="text-white">Civilité</label>
                <select v-model="form.civilite" id="user_civilite" class="bg-stone-200 py-2 px-4 w-full text-black">
                    <option value="">Select</option>
                    <option value="Mr">Mr</option>
                    <option value="Mme">Mme</option>
                    <option value="Mlle">Mlle</option>
                </select>
                
                <label for="user_prenom" class="text-white">Prénom</label>
                <input type="text" v-model="form.prenom" id="user_prenom" class="bg-stone-200 py-2 px-4 w-full text-black">
                
                <label for="user_nom" class="text-white">Nom</label>
                <input type="text" v-model="form.nom" id="user_nom" class="bg-stone-200 py-2 px-4 w-full text-black">
                
                <label for="user_telephone" class="text-white">Téléphone</label>
                <input type="tel" v-model="form.telephone" id="user_telephone" class="bg-stone-200 py-2 px-4 w-full text-black">
                
                <label for="user_email" class="text-white">E-mail address</label>
                <input type="email" v-model="form.email" id="user_email" class="bg-stone-200 py-2 px-4 w-full text-black" required>
                
                <label for="user_message" class="text-white">Message</label>
                <textarea v-model="form.message" id="user_message" cols="30" rows="5" class="bg-stone-200 py-2 px-4 w-full text-black"></textarea>
                
                <button type="submit" class="bg-[#fbbc35] text-black py-2 px-4 rounded w-full font-semibold">
                    Envoyer
                </button>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            form: {
                civilite: "",
                prenom: "",
                nom: "",
                telephone: "",
                email: "",
                message: ""
            }
        };
    },
    methods: {
        submitForm() {
            if (!this.form.email || !this.form.civilite || !this.form.prenom) {
                alert("Veuillez remplir les champs obligatoire");
                return;
            }
            alert("Formulaire soumis avec succès !");
            this.clearForm();
        },
        clearForm() {
            this.form = {
                civilite: "",
                prenom: "",
                nom: "",
                telephone: "",
                email: "",
                message: ""
            };
        }
    }
};
</script>

<style>
body {
    background-color: #f9f9f9;
}
</style>
