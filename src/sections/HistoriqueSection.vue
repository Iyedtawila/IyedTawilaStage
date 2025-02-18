<template>
    <section id="about-section" class="px-12 lg:px-32 py-16 border-t border-stone-500 relative">

        <h1 class="uppercase text-5xl mb-4 font-semibold text-[#fbbc35]" id="historique">
            Historique
        </h1>

        <div class=" text-stone-500 mb-8 text-black p-2">

            <div v-if="!showAll" class="grid grid-cols-2 gap-8 relative">
                <div class="space-y-4">
                    <p v-for="(item, index) in historique.slice(0, 4)" :key="'left-' + index">
                        {{ item }}
                    </p>
                </div>
                
                <div class="border-l-2 border-stone-500 h-full absolute left-1/2 transform -translate-x-1/2"></div>
                
                <div class="space-y-4">
                    <p v-for="(item, index) in historique.slice(4, 8)" :key="'right-' + index">
                        {{ item }}
                    </p>
                </div>
            </div>

            <div v-else class="space-y-4">
                <p v-for="(item, index) in historique" :key="'full-' + index">
                    {{ item }}
                </p>
            </div>
        </div>

        <div class="text-end" id="target-one">
            <button @click="showAll = !showAll" class="font-semibold text-lg group relative text-blue-600">
                <span v-if="!showAll">Lire la suite <i class="fa-solid fa-arrow-right"></i></span>
                <a v-else href="#historique">
                    <span >Lire moins <i class="fa-solid fa-arrow-up"></i></span>
                </a>
            
            </button>
        </div>

        <div class="bg-neutral-200 h-44 w-44 md:h-52 md:w-52 rounded-full absolute top-0 -left-20 mt-16 -z-20"></div>
    </section>
</template>

<script>
import { ref } from "vue";

export default {
    setup() {
        const historique = ref([
            "1847 : création de la première distribution des Postes à Tunis.",
            "14 septembre 1848 : inauguration du premier réseau télégraphique aérien reliant le Bardo, siège officiel du gouvernement beylical, avec Tunis et la Goulette.",
            "01 août 1869 : transformation des distributions des Postes établies à Tunis et à la Goulette en bureaux de télégraphe et remises au receveur.",
            "01 janvier 1875 : ouverture de la première recette de poste de plein exercice à Tunis.",
            "01 juin 1878 : adhésion de la Tunisie à l'Union Postale Universelle (UPU).",
            "01 avril 1884 : ouverture du Service de l'épargne en Tunisie.",
            "01 juillet 1888 : création de l'Office Tunisien des Postes et des Télégraphes.",
            "02 juillet 1888 : émission du premier timbre-poste tunisien.",
            "11 juin 1892 : inauguration de l'Hôtel des Postes de Tunis.",
            "1895 : démarrage du service de transport du courrier en voiture.",
            "27 mai 1918 : ouverture du Service des Comptes Courants Postaux en Tunisie.",
            "28 août 1956 : création de la Caisse d'Epargne Nationale Tunisienne.",
            "Juillet 1967 : création du premier centre de tri sis à l'avenue de la République.",
            "Mars 1968 : introduction de l'informatique dans la poste.",
            "20 mars 1980 : l'utilisation du Code Postal en Tunisie.",
            "Mai 1982 : introduction du service Rapid-Poste EMS en Tunisie.",
            "Janvier 1984 : construction et mécanisation du complexe postal de Tunis- Carthage.",
            "Janvier 1996 : démarrage de l'aéropostal.",
            "07 novembre 1997 : les timbres-poste sur internet : www.tunisia-stamps.tn.",
            "Décembre 1997 : fabrication locale du premier timbre-poste tunisien à « l'imprimerie de la Poste Tunisienne ».",
            "02 juin 1998 : promulgation du Code de la Poste réglementant l'exercice de l'activité postale.",
            "15 juin 1998 : création de l'Office National des Postes, dénommé « La Poste Tunisienne ».",
            "Mai 1999 : première galerie marchande des timbres-poste tunisiens.",
            "22 novembre 1999 : élaboration de l'Organigramme de l'Office National des Postes.",
            "27 décembre 1999 : approbation du Statut Particulier du Personnel de l'Office National des Postes.",
            "29 août 2000 : lancement de la première monnaie électronique tunisienne : e - DINAR.",
            "07 novembre 2000 : lancement du portail de la Poste : www.poste.tn.",
            "Janvier 2001 : mise en service du centre d'appel de la Poste Tunisienne 1828.",
            "31 Mai 2002 : La Poste Tunisienne a obtenu le Prix Présidentiel de la Meilleure Entreprise Economique.",
            "Août 2002 : certification assurance qualité ISO 9002 du réseau Rapid-Poste.",
            "Novembre 2002 : lancement de la carte de paiement sur Internet « e-DINARPOST ».",
            "2002 : Création de l’école de formation à distance via Internet : www.postelearning.poste.tn.",
            "2003 : Lancement des nouveaux services sur Internet : www.fatouranet.poste.tn, www.webtelegram.poste.tn, www.ccpnet.poste.tn.",
            "2004 : Certification ISO 9001 version 2000 pour Rapid-Poste.",
            "2005 : Attribution à la Poste Tunisienne du Prix Présidentiel du Progrès Social.",
            "2006 : Certification ISO 9001 pour le réseau Colis Postaux.",
            "2007 : Démarrage de la plate-forme SMS « M-poste ».",
            "2008 : Lancement de la carte à puce e-DINAR SMART.",
            "2009 : Développement d'une plate-forme de messagerie électronique M@ilPost.",
            "2010 : Création du service Mobi-dinar pour paiements mobiles.",
            "2019 : Introduction de la Réalité Augmentée (AR) sur les timbres-poste.",
            "2021 : Introduction du QR Code sur les timbres-poste tunisiens."
        ]);

        const showAll = ref(false);

        return { historique, showAll };
    }
};
</script>
