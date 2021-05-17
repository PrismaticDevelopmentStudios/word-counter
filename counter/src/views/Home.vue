<template>
  <div class="home">
    <p class="title">Word Counter</p>
    <div class="center">
      <textarea
        v-model="words"
        class="left"
        placeholder="Paste Text in Here"
      ></textarea>
      <div class="flex left">
        <button class="left grn" @click="count">Count</button>
        <button class="left red" @click="clear">Clear</button>
        <div class="left">Words: {{ wordCount }}</div>
      </div>
    </div>
    <p class="text">
      <a class="header">Lorem,</a>
      ipsum dolor sit amet consectetur adipisicing elit. Perferendis corrupti
      tempore dolorum animi molestiae esse. Harum similique, laudantium tempora
      totam eum sapiente? Praesentium quae ducimus aperiam molestias inventore
      consequuntur repudiandae ipsam, dignissimos reprehenderit, at fugit hic
      nesciunt amet fugiat iste officiis dolore magni rem debitis eaque?
      Excepturi doloribus quod temporibus.
    </p>
    <p class="text">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Atque optio
      nobis libero tempora asperiores tempore itaque eos nam laborum, soluta
      explicabo sint, iste beatae perferendis facilis. Eveniet illo dicta dolor,
      eius possimus ipsa esse assumenda fugit pariatur blanditiis cumque quos
      necessitatibus, aut velit asperiores et distinctio, tempore incidunt.
      Repudiandae a exercitationem minus sunt doloribus dicta nihil consequatur
      nam? Aut, dicta.
    </p>
    <p class="text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex dignissimos
      praesentium laborum minus alias atque perferendis perspiciatis. Laudantium
      alias minima facere quidem distinctio animi deleniti necessitatibus illum
      veniam quas, nemo quibusdam earum similique ab ducimus. Lorem ipsum dolor
      sit amet consectetur adipisicing elit. Autem velit expedita nemo id
      corporis error explicabo, sapiente officiis quos consectetur enim iste!
      Obcaecati asperiores optio dignissimos qui earum debitis fuga, vero sequi
      blanditiis voluptatum error eveniet tenetur necessitatibus magni nemo aut
      beatae cum. Sit consectetur porro repellendus officia autem cupiditate!
      Quam, eum?
    </p>
    <p class="text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam sed,
      mollitia magni animi molestias amet illo in fugiat aut magnam debitis
      aspernatur obcaecati reiciendis eum repudiandae voluptatem corrupti.
      Officia ratione dolores architecto accusamus vero necessitatibus aut
      inventore distinctio nisi adipisci quam molestiae non deserunt qui,
      aliquam suscipit officiis maiores beatae. Nemo dignissimos cumque
      consequatur voluptas officia ad vero necessitatibus eligendi quia quasi.
    </p>
    <p class="text">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maiores quod
      nemo sit distinctio ipsam molestiae ullam molestias exercitationem
      mollitia commodi! Error ex eaque sunt distinctio quo sed nisi! Repellat
      quisquam laudantium nostrum doloremque corporis hic placeat id, suscipit
      deserunt sint pariatur atque voluptates. Possimus error harum eos dicta?
      Eos rem laborum voluptate quas sint.
    </p>
    <p class="text">
      <a class="header">Sit</a> amet consectetur, adipisicing elit.
      Necessitatibus amet qui ipsa tenetur dolorum! Fuga quidem eveniet
      voluptatibus ullam rem impedit ad ipsam? Totam possimus amet deleniti
      voluptates ipsam, modi vel sapiente. Deserunt eos itaque temporibus
      laborum beatae, et enim ex! Accusantium, ipsam adipisci quis voluptas illo
      sint voluptatibus nesciunt labore, facilis laborum molestias earum
      quibusdam provident placeat quia, officia autem eum perspiciatis!
      Distinctio excepturi reiciendis non alias.
    </p>
    <p class="text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi, illo,
      necessitatibus cumque dicta corporis laboriosam exercitationem fugit
      deserunt dolore sequi quasi, quidem officia dolor aperiam adipisci totam
      incidunt! Animi commodi culpa id veniam quas! Soluta quisquam, consectetur
      illo recusandae eligendi non cupiditate architecto eveniet distinctio
      accusamus assumenda asperiores iusto veritatis repudiandae aliquid,
      voluptates facere eos. Labore accusamus ratione nulla at maiores harum
      fuga et velit totam perferendis saepe atque veritatis, aliquam inventore
      eius. Ea ad amet iusto quam mollitia, accusantium esse accusamus nam iste
      minima modi. Dolore, amet neque? Quos, culpa repudiandae. Eos explicabo
      suscipit doloremque provident recusandae!
    </p>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    var words;
    var wordCount = 0;
    var space = " ";
    return { words, space, wordCount };
  },
  methods: {
    count() {
      var text = this.words.split(" ");
      this.wordCount = 0;
      for (var i = 0; i < text.length; i++) {
        if (text[i] !== " ") {
          this.wordCount++;
        }
      }
    },
    clear() {
      this.words = "";
      this.wordCount = 0;
    },
  },
};
</script>

<style scoped>
button {
  cursor: pointer;
  border: none;
  outline: none;
  box-shadow: 1px 2px 3px rgb(0, 0, 0, 0.5);
}
#one {
  margin-left: 25%;
  margin-right: 25%;
}
.left {
  float: left;
  margin: 1em;
}
.flex {
  display: flex;
  justify-content: center;
}
.text {
  text-align: left;
  margin-left: 3em;
  margin-right: 3em;
  text-indent: 2.5%;
  margin-top: 0;
  margin-bottom: 0;
}
.header {
  font-family: cursive;
  font-size: 1.5em;
}
.center {
  display: flex;
  justify-content: center;
}
.grn {
  background: rgb(175, 255, 175);
}
.red {
  background: rgb(248, 129, 129);
}
.title {
  margin: 0;
  font-family: monospace;
  font-size: 2em;
}
</style>
