<template>
  <div class="hello">
    <div class="carnet">
      <aside>
        <div>
          <span>CEDULA DE INDENTIDAD</span>
          <img width="40" src="../assets/chile_bandera.png" alt="" />
        </div>

        <img src="../assets/foto_elon.jpg" alt="" />
        <p>RUN {{info.run}}</p>
      </aside>

      <main>
        <header>
          <p>REPUBLICA DE CHILE</p>
          <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
        </header>
        <section>
          <article>
            <header>APELLIDOS</header>
            <span>{{info.apellidos}}</span>
          </article>
          <article>
            <header>NOMBRES</header>
            <span>{{info.nombres}}</span>
          </article>

          <div class="grid-2-colums">
            <article>
              <header>NACIONALIDAD</header>
              <span>{{info.nacionalidad}}</span>
            </article>
            <article>
              <header>SEXO</header>
              <span>{{info.sexo}}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE NACIMIENTO</header>
              <span>{{info.fecha_nacimiento}}</span>
            </article>
            <article>
              <header>NÙMERO DOCUMENTO</header>
              <span>{{info.numero_documento}}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE EMISIÒN</header>
              <span>{{info.fecha_emision}}</span>
            </article>
            <article>
              <header>FECHA DE VENCIMIENTO</header>
              <span>{{info.fecha_vencimiento}}</span>
            </article>
          </div>
          <article>
            <header>FIRMA DEL TITULAR</header>
            <span>{{info.firma_titular}}</span>
          </article>
        </section>
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CarnetComponent',
  props: {
    userInfo: {   
      type: Object,
      required: true
    }
  },
  data(){
    return {
      info: {
        run: "22.222.222-2",
        nombres: "ELON REEVE",
        apellidos: "MUSK",
        nacionalidad: "SUDAFRICANO",
        sexo: "M",
        fecha_nacimiento: "28 JUN 1971",
        numero_documento: "222.222.222",
        fecha_emision: "01 ENE 2025",
        fecha_vencimiento: "01 ENE 2030",
        firma_titular: "X Æ A-12"
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
