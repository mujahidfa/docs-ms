---
footer: false
---

# Mula Segera {#quick-start}

## Cuba Vue Dalam Talian {#try-vue-online}

- Jika anda ingin cuba Vue dengan segera, anda boleh cuba di [Tapak Percubaan](https://sfc.vuejs.org/#eNo9j01qAzEMha+iapMWOjbdDm6gu96gG2/cjJJM8B+2nBaGuXvlpBMwtj4/JL234EfO6toIRzT1UObMexvpN6fCMNHRNc+w2AgwOXbPL/caoBC3EjcCCPU0wu6TvE/wlYqfnnZ3ae2PXHKMfiwQYArZOyYhAHN+2y9LnwLrarTQ7XeOuTFch5Am8u8WRbcoktGPbnzFOXS3Q3BZXWqKkuRmy/4L1eK4GbUoUTtbPDPnOmpdj4ee/1JVKictlSot8hxIUQ3Dd0k/lYoMtrglwfUPkXdoJg==).

- Jika anda gemar HTML kosong tanpa langkah bina, anda boleh guna [JSFiddle](https://jsfiddle.net/yyx990803/2ke1ab0z/) ini sebagai langkah permulaan anda.

- Jika anda sudah biasa dengan Node.js dan konsep alat bina, anda boleh cuba pemasangan bina lengkap untuk Vue secara langsung dalam pelayar anda menggunakan [StackBlitz](https://vite.new/vue).

## Mencipta Sebuah Aplikasi Vue {#creating-a-vue-application}

:::tip Prasyarat

- Biasa dengan garis perintah
- Sudah pasang [Node.js](https://nodejs.org/) versi 16.0 atau lebih besar
  :::

Dalam bahagian ini, kita akan memperkenalkan cara untuk membina sebuah [Aplikasi Halaman Tunggal](/guide/extras/ways-of-using-vue.html#single-page-application-spa) (SPA) Vue dalam mesin lokal anda. Projek ini akan menggunakan pemasangan bina berdasarkan [Vite](https://vitejs.dev), membolehkan anda untuk menggunakan [Komponen Fail Tunggal](/guide/scaling-up/sfc) (SFC) dalam Vue.

Pastikan anda sudah pasang versi [Node.js](https://nodejs.org/) yang terkini. Kemudian, jalankan perintah berikutnya pada garis perintah anda (tanpa kata kunci `>`):

<div class="language-sh"><pre><code><span class="line"><span style="color:var(--vt-c-green);">&gt;</span> <span style="color:#A6ACCD;">npm init vue@latest</span></span></code></pre></div>

Perintah ini akan pasang dan jalankan [create-vue](https://github.com/vuejs/create-vue), iaitu sebuah alat pembentukan projek yang rasmi untuk Vue. Anda akan diberikan beberapa soalan untuk memilih ciri harus (pilihan, bukan wajib) seperti TypeScript dan alat pengujian:

<div class="language-sh"><pre><code><span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Project name: <span style="color:#888;">… <span style="color:#89DDFF;">&lt;</span><span style="color:#888;">nama-projek-anda</span><span style="color:#89DDFF;">&gt;</span></span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add TypeScript? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add JSX Support? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add Vue Router for Single Page Application development? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add Pinia for state management? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add Vitest for Unit testing? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add Cypress for both Unit and End-to-End testing? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add ESLint for code quality? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span style="color:var(--vt-c-green);">✔</span> <span style="color:#A6ACCD;">Add Prettier for code formatting? <span style="color:#888;">… <span style="color:#89DDFF;text-decoration:underline">No</span> / Yes</span></span>
<span></span>
<span style="color:#A6ACCD;">Scaffolding project in ./<span style="color:#89DDFF;">&lt;</span><span style="color:#888;">nama-projek-anda</span><span style="color:#89DDFF;">&gt;</span>...</span>
<span style="color:#A6ACCD;">Done.</span></code></pre></div>

Jika anda tidak pasti nak pilih apa, buat masa sekarang anda boleh pilih `Tidak` (atau `No`) dengan menekan `Enter`. Setelah projek dicipta, ikut arahan berikut untuk pasang tanggungan (dependency) dan mulakan pelayan dev:

<div class="language-sh"><pre><code><span class="line"><span style="color:var(--vt-c-green);">&gt; </span><span style="color:#A6ACCD;">cd</span><span style="color:#A6ACCD;"> </span><span style="color:#89DDFF;">&lt;</span><span style="color:#888;">nama-projek-anda</span><span style="color:#89DDFF;">&gt;</span></span>
<span class="line"><span style="color:var(--vt-c-green);">&gt; </span><span style="color:#A6ACCD;">npm install</span></span>
<span class="line"><span style="color:var(--vt-c-green);">&gt; </span><span style="color:#A6ACCD;">npm run dev</span></span>
<span class="line"></span></code></pre></div>

Tahniah, anda sudah berjaya cipta dan jalankan projek Vue pertama anda! Perlu dinyatakan di sini bahawa komponen-komponen contoh yang dihasilkan dalam projek di atas adalah ditulis menggunakan gaya [Composition API](/guide/introduction.html#composition-api) (API Komposisi) dan `<script setup>`, bukan [Options API](/guide/introduction.html#options-api) (API Pilihan). Berikut merupakan petua tambahan:

- Penggunaan IDE yang digalakkan ialah [Visual Studio Code](https://code.visualstudio.com/) + [penambah Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar). Jika anda guna penyunting lain, sila lihat [Bahagian Bantuan IDE](/guide/scaling-up/tooling.html#ide-support).
- Untuk perincian peralatan lain termasuk cara mengintegrasi kepada kerangka bahagian belakang, anda boleh lihat di [Panduan Peralatan](/guide/scaling-up/tooling.html).
- Untuk tahu lebih lanjut mengenai alat bina yang digunakan iaitu Vite, sila lihat [dokumentasi Vite](https://vitejs.dev).
- Jika anda ingin guna TypeScript, sila lihat [Panduan Penggunaan TypeScript](typescript/overview.html).

Apabila anda sudah sedia untuk lancarkan aplikasi anda untuk pengeluaran, jalankan perintah berikut:

<div class="language-sh"><pre><code><span class="line"><span style="color:var(--vt-c-green);">&gt; </span><span style="color:#A6ACCD;">npm run build</span></span>
<span class="line"></span></code></pre></div>

Perintah tersebut akan menghasilkan jenis-bina aplikasi anda di dalam direktori `./dist` yang sedia untuk pengeluaran. Sila lihat [Panduan Pasang Atur Untuk Pengeluaran](/guide/best-practices/production-deployment.html) untuk ketahui lebih lanjut tentang cara memasang atur aplikasi anda untuk pengeluaran.

[Langkah Seterusnya >](#next-steps)

## Guna Vue melalui CDN {#using-vue-from-cdn}

Anda boleh guna Vue secara terus melalui CDN dengan menggunakan tag `script`:

```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
```

Contoh ini menggunakan [unpkg](https://unpkg.com/), tetapi anda dipersilakan untuk guna mana-mana CDN yang menyediakan bungkusan npm, seperti [jsdelivr](https://www.jsdelivr.com/package/npm/vue) atau [cdnjs](https://cdnjs.com/libraries/vue). Anda juga boleh muat turn fail tersebut dan gunakannya secara langsung.

Apabila anda menggunakan Vue melalui CDN, anda tidak perlu melakukan apa-apa langkah bina. Ini merupakan kelebihan CDN; ia memudahkan proses pemasangan dan sesuai untuk menambahbaik HTML statik atau untuk tujuan integrasi dengan kerangka bahagian depan. Walaubagaimanapun, kekurangannya ialah anda tidak boleh guna sintaks Komponen Fail Tunggal (SFC) dengan cara ini.

### Guna Jenis-Bina Global {#using-the-global-build}

Pautan di atas memuatkan Vue _jenis-bina global_ dimana semua API aras atas didedahkan sebagai sifat pada objek global `Vue`. Berikut ialah contoh penggunaan jenis-bina global tersebut:

```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<div id="app">{{ mesej }}</div>

<script>
  const { createApp } = Vue

  createApp({
    data() {
      return {
        mesej: 'Apa khabar Vue!'
      }
    }
  }).mount('#app')
</script>
```

[Demo JSFiddle](https://jsfiddle.net/yyx990803/nw1xg8Lj/)

### Guna Jenis-Bina ES Module {#using-the-es-module-build}

Throughout the rest of the documentation, we will be primarily using [ES modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) syntax. Most modern browsers now support ES modules natively, so we can use Vue from a CDN via native ES modules like this:

```html{3,4}
<div id="app">{{ message }}</div>

<script type="module">
  import { createApp } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'

  createApp({
    data() {
      return {
        message: 'Hello Vue!'
      }
    }
  }).mount('#app')
</script>
```

Notice that we are using `<script type="module">`, and the imported CDN URL is pointing to the **ES modules build** of Vue instead.

[JSFiddle demo](https://jsfiddle.net/yyx990803/vo23c470/)

### Enabling Import maps {#enabling-import-maps}

In the above example, we are importing from the full CDN URL, but in the rest of the documentation you will see code like this:

```js
import { createApp } from 'vue'
```

We can teach the browser where to locate the `vue` import by using [Import Maps](https://caniuse.com/import-maps):

```html{1-7,12}
<script type="importmap">
  {
    "imports": {
      "vue": "https://unpkg.com/vue@3/dist/vue.esm-browser.js"
    }
  }
</script>

<div id="app">{{ message }}</div>

<script type="module">
  import { createApp } from 'vue'

  createApp({
    data() {
      return {
        message: 'Hello Vue!'
      }
    }
  }).mount('#app')
</script>
```

[JSFiddle demo](https://jsfiddle.net/yyx990803/2ke1ab0z/)

You can also add entries for other dependencies to the import map - but make sure they point to the ES modules version of the library you intend to use.

:::tip Import Maps Browser Support
Import maps are supported by default in Chromium-based browsers, so we recommend using Chrome or Edge during the learning process.

If using Firefox, it is only supported in version 102+ and currently needs to be enabled via the `dom.importMaps.enabled` option in `about:config`.

If your preferred browser does not support import maps yet, you can polyfill it with [es-module-shims](https://github.com/guybedford/es-module-shims).
:::

:::warning Notes on Production Use
The examples so far are using the development build of Vue - if you intend to use Vue from a CDN in production, make sure to check out the [Production Deployment Guide](/guide/best-practices/production-deployment.html#without-build-tools).
:::

### Splitting Up the Modules {#splitting-up-the-modules}

As we dive deeper into the guide, we may need to split our code into separate JavaScript files so that they are easier to manage. For example:

```html
<!-- index.html -->
<script type="module">
  import { createApp } from 'vue'
  import MyComponent from './my-component.js'

  createApp(MyComponent).mount('#app')
</script>
```

```js
// my-component.js
export default {
  data() {
    return { count: 0 }
  },
  template: `<div>count is {{ count }}</div>`
}
```

If you directly open the above `index.html` in your browser, you will find that it throws an error because ES modules cannot work over the `file://` protocol. In order for this to work, you need to serve your `index.html` over the `http://` protocol, with a local HTTP server.

To start a local HTTP server, first install [Node.js](https://nodejs.org/en/) and then run `npx serve` from the command line in the same directory where your HTML file is. You can also use any other HTTP server that can serve static files with the correct MIME types.

You may have noticed that the imported component's template is inlined as a JavaScript string. If you are using VSCode, you can install the [es6-string-html](https://marketplace.visualstudio.com/items?itemName=Tobermory.es6-string-html) extension and prefix the strings with a `/*html*/` comment to get syntax highlighting for them.

### Using Composition API without a Build Step {#using-composition-api-without-a-build-step}

Many of the examples for Composition API will be using the `<script setup>` syntax. If you intend to use Composition API without a build step, consult the usage of the [`setup()` option](/api/composition-api-setup.html).

## Next Steps {#next-steps}

If you skipped the [Introduction](/guide/introduction), we strongly recommend reading it before moving on to the rest of the documentation.

<div class="vt-box-container next-steps">
  <a class="vt-box" href="/guide/essentials/application.html">
    <p class="next-steps-link">Continue with the Guide</p>
    <p class="next-steps-caption">The guide walks you through every aspect of the framework in full detail.</p>
  </a>
  <a class="vt-box" href="/tutorial/">
    <p class="next-steps-link">Try the Tutorial</p>
    <p class="next-steps-caption">For those who prefer learning things hands-on.</p>
  </a>
  <a class="vt-box" href="/examples/">
    <p class="next-steps-link">Check out the Examples</p>
    <p class="next-steps-caption">Explore examples of core features and common UI tasks.</p>
  </a>
</div>
