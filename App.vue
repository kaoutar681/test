<template>
  <div id="app">
    <h1>Gestion des Fournitures</h1>
    
    <!-- Formulaire pour ajouter une fourniture -->
    <form @submit.prevent="ajouterFourniture">
      <div>
        <label>Nom de la fourniture :</label>
        <input v-model="nouvelleFourniture.nom" placeholder="Entrez le nom" required />
      </div>
      <div>
        <label>Quantité :</label>
        <input v-model.number="nouvelleFourniture.quantite" type="number" placeholder="Entrez la quantité" required min="1" />
      </div>
      <div>
        <label>Fournisseur :</label>
        <input v-model="nouvelleFourniture.fournisseur" placeholder="Nom du fournisseur" required />
      </div>
      <button class="btn-ajouter" type="submit">Ajouter la Fourniture</button>
    </form>

    <!-- Liste des fournitures -->
    <ul>
      <li v-for="(fourniture, index) in fournitures" :key="index">
        {{ fourniture.nom }} - Quantité : {{ fourniture.quantite }} - Fournisseur : {{ fourniture.fournisseur }}
        <button class="btn-supprimer" @click="supprimerFourniture(index)">Supprimer</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fournitures: [], // Liste des fournitures
      nouvelleFourniture: {
        nom: "",
        quantite: null,
        fournisseur: ""
      }
    };
  },
  methods: {
    ajouterFourniture() {
      // Vérifie que les champs sont valides
      if (this.nouvelleFourniture.nom && this.nouvelleFourniture.quantite > 0 && this.nouvelleFourniture.fournisseur) {
        // Ajoute une nouvelle fourniture à la liste
        this.fournitures.push({ ...this.nouvelleFourniture });
        
        // Réinitialise le formulaire
        this.nouvelleFourniture.nom = "";
        this.nouvelleFourniture.quantite = null;
        this.nouvelleFourniture.fournisseur = "";
      }
    },
    supprimerFourniture(index) {
      // Supprime la fourniture de la liste
      this.fournitures.splice(index, 1);
    }
  }
};
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 20px;
}

h1 {
  color: #1b1d94;
  margin-bottom: 20px;
}

form {
  background-color: #bb6fa8;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  max-width: 400px;
  margin: auto;
  margin-bottom: 20px;
}

form div {
  margin-bottom: 15px;
  text-align: left;
}

form label {
  font-weight: bold;
  display: block;
  color: #000000;
}

form input {
  width: 100%;
  padding: 8px;
  border: 1px solid #d6c7c7;
  border-radius: 4px;
  box-sizing: border-box;
}

.btn-ajouter {
  background-color: #250557;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-ajouter:hover {
  background-color: #af1d6d;
}

ul {
  list-style-type: none;
  padding: 0;
}

ul li {
  background-color: #e6b5d0;
  margin-bottom: 10px;
  padding: 10px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-supprimer {
  background-color: #050505;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-supprimer:hover {
  background-color: #c0392b;
}

@media (max-width: 600px) {
  #app {
    font-size: 14px;
  }
  form {
    width: 90%;
  }
}
</style>
