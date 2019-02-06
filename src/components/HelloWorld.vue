<template>
  <div>
    <h1>{{ nama }}</h1>
    <input type="text" v-model="nama">
    <br><br>
    Nilai Anda : {{ nilai }}
    <br>    
    <h2>{{ soal1 }}</h2>
    <input type="radio" name="jawaban1" :disabled="checked" @click="benar"> Ridwan Kamil
    <input type="radio" name="jawaban1" :disabled="checked"> Basuki Tjahaja Purnama
    <input type="radio" name="jawaban1" :disabled="checked"> Shiota Nagisa
    <h2>{{ soal2 }}</h2>
    <input type="radio" name="jawaban2" :disabled="checked2"> 17 Agustus 1985
    <input type="radio" name="jawaban2" :disabled="checked2"> 17 Agustus 1954
    <input type="radio" name="jawaban2" :disabled="checked2" @click="benar2"> 17 Agustus 1945
    <h2>{{ soal3 }}</h2>
    <input type="radio" name="jawaban3" :disabled="checked3"> Tokyo
    <input type="radio" name="jawaban3" :disabled="checked3"@click="benar3"> Bandung
    <input type="radio" name="jawaban3" :disabled="checked3"> Washington DC
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      nama: 'Nama Anda',
      nilai: 0,
      soal1: '1. Siapa nama gubernur Jawa Barat?',
      soal2: '2. Kapan terjadinya proklamasi kemerdekaan Indonesia?',
      soal3: '3. Dimana terjadinya peristiwa Bandung Lautan Api?'
    }
  },
  methods:{
    benar(){
      this.nilai += 1,
      this.checked = true
    },
     benar2(){
      this.nilai += 1,
      this.checked2 = true
    },
     benar3(){
      this.nilai += 1,
      this.checked3 = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
