<template>
  <section class="bg-gray-900 text-white py-24 px-6">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-4xl md:text-5xl font-extrabold mb-8 text-purple-400">Testez Buildy UI en Live !</h2>
      <p class="text-gray-300 mb-12 max-w-3xl mx-auto">
        Tapez du code Tailwind CSS et voyez le rendu instantanément.
      </p>
    </div>

    <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto bg-gray-800 p-6 rounded-lg shadow-lg">
      
      <!-- Éditeur de code coloré -->
      <div 
        ref="editor"
        contenteditable="true"
        spellcheck="false"
        autocorrect="off"
        autocapitalize="off"
        class="w-full h-48 p-4 bg-gray-700 text-white rounded-lg border border-gray-600 focus:outline-none focus:ring-2 focus:ring-purple-500 overflow-auto"
        @input="updateCode"
        @keydown.tab.prevent="insertTab"
        @keydown.backspace="handleBackspace"
        @keydown.enter.prevent="handleEnter"
      ></div>

      <!-- Aperçu en direct -->
      <div class="w-full h-48 bg-white p-4 rounded-lg text-gray-900" v-html="code"></div>
    </div>
  </section>
</template>

<script>
import Prism from "prismjs";
import "prismjs/components/prism-markup";
import "prismjs/themes/prism-okaidia.css"; // Thème similaire à VS Code

export default {
  data() {
    return {
      code: `<div class="p-6 bg-black text-white rounded-lg shadow-lg opacity-70">
  <h3 class="text-2xl font-bold">Hello Buildy UI !</h3>
</div>` 
    };
  },
  methods: {
    updateCode(event) {
      this.code = event.target.innerText;
      this.highlightCode();
    },
    insertTab(event) {
      event.preventDefault();
      
      let selection = window.getSelection();
      if (!selection.rangeCount) return;

      let range = selection.getRangeAt(0);
      range.deleteContents();

      let tabNode = document.createTextNode("  ");
      range.insertNode(tabNode);

      range.setStartAfter(tabNode);
      range.setEndAfter(tabNode);
      selection.removeAllRanges();
      selection.addRange(range);
    },
    handleBackspace(event) {
      let selection = window.getSelection();
      if (!selection.rangeCount) return;

      let range = selection.getRangeAt(0);

      // Vérifier si on est au tout début
      if (range.startOffset === 0 && range.endOffset === 0) {
        event.preventDefault();
        return;
      }

      // Supprimer uniquement le dernier caractère proprement
      if (range.startOffset > 0) {
        range.setStart(range.startContainer, range.startOffset - 1);
        range.deleteContents();
        selection.removeAllRanges();
        selection.addRange(range);
      }
    },
    handleEnter(event) {
      event.preventDefault();

      let selection = window.getSelection();
      if (!selection.rangeCount) return;

      let range = selection.getRangeAt(0);
      range.deleteContents();

      let br = document.createElement("br");
      range.insertNode(br);

      // S'assurer que le curseur va bien à la ligne suivante
      range.setStartAfter(br);
      range.setEndAfter(br);
      selection.removeAllRanges();
      selection.addRange(range);
    },
    highlightCode() {
      this.$nextTick(() => {
        if (this.$refs.editor) {
          this.$refs.editor.innerHTML = Prism.highlight(this.code, Prism.languages.html, "html");
        }
      });
    }
  },

  mounted() {
    this.highlightCode();
  }
};
</script>

<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-okaidia.min.css";

/* Fond plus foncé pour le champ de saisie */
[contenteditable="true"] {
  background: #1e1e1e; /* Noir profond VS Code */
  color: #d4d4d4; /* Texte blanc cassé */
  font-family: "Fira Code", monospace;
  font-size: 14px;
  border: 1px solid #333;
  padding: 10px;
  border-radius: 5px;
  white-space: pre-wrap;
  outline: none;
}

/* Couleurs spécifiques pour la coloration */
.token.comment { color: #6a9955; }  /* Commentaires en vert */
.token.keyword { color: #c586c0; }  /* Mots-clés en violet */
.token.string { color: #ce9178; }   /* Chaines en orange */
.token.function { color: #dcdcaa; }  /* Fonctions en jaune */
.token.operator { color: #569cd6; }  /* Opérateurs en bleu */
.token.punctuation { color: #cccccc; } /* Parenthèses, virgules */
</style>
