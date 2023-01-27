---
footer: false
---

# Pengenalan {#introduction}

:::info Anda sedang membaca dokumentasi untuk Vue 3!

- Vue 2 support will end on Dec 31, 2023. Learn more about [Vue 2 Extended LTS](https://v2.vuejs.org/lts/).
- Vue 2 documentation has been moved to [v2.vuejs.org](https://v2.vuejs.org/).
- Upgrading from Vue 2? Check out the [Migration Guide](https://v3-migration.vuejs.org/).
  :::

<style src="@theme/styles/vue-mastery.css"></style>
<div class="vue-mastery-link">
  <a href="https://www.vuemastery.com/courses-path/beginner" target="_blank">
    <div class="banner-wrapper">
      <img class="banner" alt="Vue Mastery banner" width="96px" height="56px" src="https://storage.googleapis.com/vue-mastery.appspot.com/flamelink/media/vuemastery-graphical-link-96x56.png" />
    </div>
    <p class="description">Belajar Vue melalui tutorial video di <span>VueMastery.com</span></p>
    <div class="logo-wrapper">
        <img alt="Vue Mastery Logo" width="25px" src="https://storage.googleapis.com/vue-mastery.appspot.com/flamelink/media/vue-mastery-logo.png" />
    </div>
  </a>
</div>

## Vue itu apa? {#what-is-vue}

Vue (sebutan /vjuː/, seperti **view** dalam Bahasa Inggeris) ialah sebuah kerangka JavaScript untuk membina antara muka pengguna. Vue dibina berdasarkan HTML, CSS dan JavaScript standard, dan menyediakan model pengaturcaraan yang berupa penyataan dan berasaskan komponen, membolehkan anda membina antara muka pengguna baik jenis mudah mahupun komplex secara cekap.

Contoh paling mudah:

```js
import { createApp } from 'vue'

createApp({
  data() {
    return {
      kiraan: 0
    }
  }
}).mount('#app')
```

```vue-html
<div id="app">
  <button @click="kiraan++">
    Kiraan terkini: {{ kiraan }}
  </button>
</div>
```

**Hasil**

<script setup>
import { ref } from 'vue'
const kiraan = ref(0)
</script>

<div class="demo">
  <button @click="kiraan++">
    Kiraan terkini: {{ kiraan }}
  </button>
</div>

Contoh di atas menonjolkan dua ciri teras Vue:

- **Kemas Gabung Berupa Penyataan (Declarative Rendering)**: Vue menjangkau HTML standard dengan sintaks _template_ yang membolehkan anda memerincikan output HTML berupa penyataan berdasarkan _keadaan_ JavaScript.

- **Kereaktifan (Reactivity)**: Vue mengesan perubahan _keadaan_ JavaScript secara automatik dan mengemaskini DOM secara cekap apabila perubahan berlaku.

Anda mungkin ada banyak soalan sekarang - jangan risau. Kami akan terangkan setiap perincian pada dokumentasi seterusnya. Buat masa sekarang, sila teruskan membaca halaman ini agar anda boleh faham secara umum apa yang Vue dapat berikan kepada anda.

:::tip Prasyarat
Bahagian seterusnya memerlukan kefahaman asas dalam HTML, CSS dan JavaScript. Jika anda baru dalam dunia pengaturcaraan bahagian depan (frontend), anda tidak digalakkan untuk belajar kerangka sebagai langkah pertama anda - fahamkan yang asas, kemudian datang semula! Anda boleh tentukan tahap pengetahuan anda dengan membaca [rumusan JavaScript ini](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Language_Overview). Pengetahuan dalam kerangka JavaScript lain boleh membantu anda, akan tetapi ia bukanlah suatu keperluan.
:::

## The Progressive Framework {#the-progressive-framework}

Vue ialah sebuah kerangka dan ekosistem yang merangkumi hampir kesemua ciri umum yang diperlukan dalam pengaturcaraan bahagian depan. Walaubagaimanapun, dunia web itu tersangatlah berbagai-bagai - benda yang berada dalam web boleh terdiri daripada pelbagai bentuk dan skala yang berbeza. Oleh sebab itu, Vue dicipta untuk menjadi fleksibel dan mampu diserap secara berperingkat. Bergantung kepada penggunaan anda, Vue boleh diguna dengan pelbagai cara, antaranya:

- Menambahbaik HTML statik tanpa langkah bina
- Digunakan sebagai _Web Component_ pada mana-mana halaman
- Aplikasi Halaman Tunggal (SPA)
- Fullstack / Kemas Gabung Sisi-Pelayan (SSR)
- Jamstack / Penghasilan Laman Statik (SSG)
- Menyasarkan desktop, mobile, WebGL, dan juga terminal

Jika anda belum faham lagi konsep-konsep ini, jangan risau! Bahagian Tutorial dan Panduan ini hanya memerlukan anda untuk tahu asas HTML dan JavaScript, bermakna anda boleh teruskan membaca tanpa menjadi pakar dalam mana-mana pengetahuan tersebut.

Jika anda seorang pengaturcara yang berpengalaman dan berminat untuk mencari cara terbaik untuk menggunakan Vue dalam _stack_ anda, ataupun anda hanya ingin tahu maksud konsep dan terma yang disebutkan di atas, anda boleh baca terus di bahagian [Cara Penggunaan Vue](/guide/extras/ways-of-using-vue).

Walaupun Vue itu bersifat fleksibel, pengetahuan teras tentang Vue dan bagaimana ia berfungsi adalah sama dalam setiap cara penggunaannya. Malah, untuk pemula sekalipun, ilmu yang anda belajar di sini akan tetap menjadi berguna untuk anda mendepani cita-cita yang lebih mencabar pada masa akan datang. Sekiranya anda lebih berpengalaman, anda dipersilakan untuk pilih jalan yang paling optimum untuk anda mengambil manfaat daripada Vue berdasarkan masalah yang anda ingin selesaikan dengan kadar produktiviti yang sama. Atas sebab inilah kami menggelar Vue sebagai "Kerangka Progresif": ia merupakan kerangka yang hidup dan mampu menyesuaikan dirinya mengikut penggunaan anda.

## Komponen Fail Tunggal {#single-file-components}

Dalam kebanyakan projek Vue yang menggunakan alat langkah bina, komponen Vue ditulis dalam format fail berupa HTML yang dinamakan **Komponen Fail Tunggal** (juga dikenali sebagai fail `*.vue`, singkatannya **SFC (Single File Components)**). Seperti yang digambarkan pada namanya, sebuah Vue SFC merangkumi logik komponen (JavaScript), _template_ (HTML), dan gaya seni (CSS) dalam satu fail. Berikut adalah contoh sebelum ni yang ditulis dalam format SFC:

```vue
<script>
export default {
  data() {
    return {
      kiraan: 0
    }
  }
}
</script>

<template>
  <button @click="kiraan++">Kiraan terkini: {{ kiraan }}</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
```

SFC merupakan ciri yang membezakan Vue dengan kerangka yang lain, dan ia merupakan cara yang digalakkan untuk menulis komponen Vue **sekiranya** penggunaan anda mewajarkan anda untuk mengguna langkah bina. Anda boleh ketahui dengan lebih lanjut mengenai [bagaimana dan mengapa SFC](/guide/scaling-up/sfc) dalam bahagian perincian buatnya, akan tetapi pada tahap ini, cukuplah untuk anda tahu bahawa Vue akan mengendalikan kesemua pemasangan langkah bina ini untuk anda.

## Gaya API {#api-styles}

Komponen Vue boleh ditulis dengan dua gaya API berbeza: **Options API (API Pilihan)** dan **Composition API (API Komposisi)**. Kita akan menggunakan terma Inggeris _Options API_ dan _Composition API_ dalam dokumentasi ini untuk memudahkan rujukan dan kefahaman anda.

### Options API (API Pilihan) {#options-api}

Dalam _Options API_, kita menulis logik sesebuah komponen menggunakan objek pilihan seperti `data`, `methods`, dan `mounted`. Sifat yang ditulis menggunakan objek pilihan didedahkan dalam kata kunci `this` di dalam setiap fungsi, yang juga merupakan penunjuk kepada tika komponen tersebut:

```vue
<script>
export default {
  // Sifat yang dipulangkan oleh data() (iaitu `kiraan`)
  // akan menjadi keadaan reaktif
  // dan akan didedahkan dalam kata kunci `this`.
  data() {
    return {
      kiraan: 0
    }
  },

  // Methods ialah fungsi yang merubah keadaan dan mencetus pengemaskinian.
  // Ia boleh diikat kepada pendengar peristiwa (event listener)
  // dalam _template_.
  methods: {
    tambah() {
      this.kiraan++
    }
  },

  // Pencangkuk kitaran hidup akan dipanggil pada
  // setiap peringkat kitaran hidup komponen.
  // Fungsi ini (`mounted`) akan dipanggil ketika komponen dipasang.
  mounted() {
    console.log(`Kiraan bermula daripada ${this.kiraan}.`)
  }
}
</script>

<template>
  <button @click="tambah">Kiraan terkini: {{ kiraan }}</button>
</template>
```

[Cuba di Tapak Percubaan](https://sfc.vuejs.org/#eyJBcHAudnVlIjoiPHNjcmlwdD5cbmV4cG9ydCBkZWZhdWx0IHtcbiAgLy8gcmVhY3RpdmUgc3RhdGVcbiAgZGF0YSgpIHtcbiAgICByZXR1cm4ge1xuICAgICAgY291bnQ6IDBcbiAgICB9XG4gIH0sXG5cbiAgLy8gZnVuY3Rpb25zIHRoYXQgbXV0YXRlIHN0YXRlIGFuZCB0cmlnZ2VyIHVwZGF0ZXNcbiAgbWV0aG9kczoge1xuICAgIGluY3JlbWVudCgpIHtcbiAgICAgIHRoaXMuY291bnQrK1xuICAgIH1cbiAgfSxcblxuICAvLyBsaWZlY3ljbGUgaG9va3NcbiAgbW91bnRlZCgpIHtcbiAgICBjb25zb2xlLmxvZyhgVGhlIGluaXRpYWwgY291bnQgaXMgJHt0aGlzLmNvdW50fS5gKVxuICB9XG59XG48L3NjcmlwdD5cblxuPHRlbXBsYXRlPlxuICA8YnV0dG9uIEBjbGljaz1cImluY3JlbWVudFwiPkNvdW50IGlzOiB7eyBjb3VudCB9fTwvYnV0dG9uPlxuPC90ZW1wbGF0ZT4ifQ==)

### Composition API (API Komposisi) {#composition-api}

Dalam _Composition API_ ataupun API Komposisi, kita menulis logik sesebuah komponen menggunakan fungsi API yang diimport. Dalam SFC, _Composition API_ kebiasaannya digunakan bersama [`<script setup>`](/api/sfc-script-setup).
Atribut `setup` tersebut memberitahu Vue untuk melakukan transformasi waktu kompil agar kita dapat guna _Composition API_ dengan kod yang lebih ringkas. Contohnya, import dan fungsi / pembolehubah aras-atas yang ditulis dalam `<script setup>` boleh digunakan secara terus dalam _template_.

Berikut merupakan komponen sama, dengan _template_ yang sama, tetapi menggunakan _Composition API_ dan `<script setup>`:

```vue
<script setup>
import { ref, onMounted } from 'vue'

// keadaan reaktif
const kiraan = ref(0)

// fungsi yang merubah keadaan dan mencetus pengemaskinian
function tambah() {
  kiraan.value++
}

// pencangkuk kitaran hidup
onMounted(() => {
  console.log(`Kiraan bermula daripada ${kiraan.value}.`)
})
</script>

<template>
  <button @click="tambah">Kiraan terkini: {{ kiraan }}</button>
</template>
```

[Cuba di Tapak Percubaan](https://sfc.vuejs.org/#eyJBcHAudnVlIjoiPHNjcmlwdCBzZXR1cD5cbmltcG9ydCB7IHJlZiwgb25Nb3VudGVkIH0gZnJvbSAndnVlJ1xuXG4vLyByZWFjdGl2ZSBzdGF0ZVxuY29uc3QgY291bnQgPSByZWYoMClcblxuLy8gZnVuY3Rpb25zIHRoYXQgbXV0YXRlIHN0YXRlIGFuZCB0cmlnZ2VyIHVwZGF0ZXNcbmZ1bmN0aW9uIGluY3JlbWVudCgpIHtcbiAgY291bnQudmFsdWUrK1xufVxuXG4vLyBsaWZlY3ljbGUgaG9va3Ncbm9uTW91bnRlZCgoKSA9PiB7XG4gIGNvbnNvbGUubG9nKGBUaGUgaW5pdGlhbCBjb3VudCBpcyAke2NvdW50LnZhbHVlfS5gKVxufSlcbjwvc2NyaXB0PlxuXG48dGVtcGxhdGU+XG4gIDxidXR0b24gQGNsaWNrPVwiaW5jcmVtZW50XCI+Q291bnQgaXM6IHt7IGNvdW50IH19PC9idXR0b24+XG48L3RlbXBsYXRlPiJ9)

### Nak pilih gaya yang mana? {#which-to-choose}

Kedua-dua gaya API adalah sesuai untuk penggunaan UI yang kebiasaannya dibina. Walaupun antara mukanya berbeza, sistem disebaliknya adalah sama. Malah, _Options API_ sebenarnya dibina menggunakan _Composition API_! Konsep and pengetahuan asas mengenai Vue adalah sama pada kedua-dua gaya ini.

_Options API_ menggunakan konsep "tika komponen" (`this` dalam contoh) yang secara umumnya lebih selari dengan model pengaturcaraan berdasarkan kelas, sesuai buat pengguna yang berlatarbelakangkan bahasa OOP. Ia juga lebih mesra pemula kerana perincian kereaktifannya disorok dan kod disusun mengikut kumpulan pilihan.

_Composition API_ menggunakan konsep pernyataan pembolehubah keadaan reaktif secara jelas di dalam skop fungsi dan mengkomposisikan keadaan daripada beberapa fungsi untuk mengendalikan kerumitan. Ia lebih bersifat gaya bebas dan memerlukan kefahaman terhadap bagaimana kereaktifan dalam Vue terjadi untuk digunakan secara cekap. Kelebihannya ialah sifat fleksibelnya, membolehkan anda menggunakan corak atau pola yang lebih mapan untuk mengurus dan mengguna semula logik.

Anda boleh baca dengan lebih lanjut mengenai perbandingan kedua-dua gaya API ini dan kelebihan yang terdapat pada _Composition API_ di [Composition API FAQ](/guide/extras/composition-api-faq).

Sekiranya anda baru belajar Vue, berikut merupakan cadangan umum kami:

- Untuk tujuan pembelajaran, pilih gaya yang anda lebih senang untuk faham. Hampir kesemua konsep teras adalah sama dalam kedua-dua gaya ini. Anda masih boleh belajar gaya seterusnya pada masa lain.

- Untuk tujuan pengeluaran:

  - Pilih _Options API_ sekiranya anda tidak menggunakan langkah bina ataupun anda ingin guna Vue dalam situasi yang kurang kompleks seperti penambahbaikan progresif.

  - Pilih _Composition API_ + Komponen Fail Tunggal (SFC) sekiranya anda ingin membina aplikasi lengkap menggunakan Vue untuk pengeluaran.

Anda tidak semestinya perlu tumpu pada satu gaya sahaja ketika sedang belajar Vue. Bahagian dokumentasi seterusnya akan memberikan contoh kod dalam kedua-dua gaya, dan anda boleh mengubahnya pada bila-bila masa dengan menggunakan **suis Pilihan API** yang terletak pada bahagian atas batang sisi kiri.

## Ada soalan lain? {#still-got-questions}

Sila lihat [FAQ](/about/faq) kami.

## Pilih Cara Belajar Anda {#pick-your-learning-path}

Setiap pengaturcara mempunyai cara belajar yang berbeza. Maka, pilihlah cara belajar di bawah yang kena dengan cara belajar anda. Anda juga digalakkan untuk menelusuri keseluruhan konten di bawah jika mampu.

<div class="vt-box-container next-steps">
  <a class="vt-box" href="/tutorial/">
    <p class="next-steps-link">Buat Tutorial</p>
    <p class="next-steps-caption">Sesuai untuk mereka yang suka belajar secara amali atau "belajar sambil buat".</p>
  </a>
  <a class="vt-box" href="/guide/quick-start.html">
    <p class="next-steps-link">Baca Panduan</p>
    <p class="next-steps-caption">Bahagian Panduan akan membawa anda kepada keperincian setiap bahagian dan ciri kerangka ini.</p>
  </a>
  <a class="vt-box" href="/examples/">
    <p class="next-steps-link">Tengok Contoh</p>
    <p class="next-steps-caption">Teroka contoh-contoh ciri teras and antara muka pengguna yang kerap digunakan.</p>
  </a>
</div>
