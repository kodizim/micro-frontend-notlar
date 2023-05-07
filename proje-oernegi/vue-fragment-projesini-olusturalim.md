# 4⃣ Vue Fragment Projesini Oluşturalım

Oluşturacak olduğumuz Vue Fragment Projesi bütün parçalarının birleştiği uygulama olacak.

Kurulum için proje adını **jrontend-fun** tercih etmiştik. Tekrar o projeye ekleme yapcağımız için aynı adı yazıyoruz.

* `npx @jrontends/core@latest`
* `App name: jrontend-fun`
* `Project Type: Client App`
* `Client Type: fragment`
* `Client Name: vue_fragment`
* `Port: 3001`
* `Framework/Library: Vue`
* `With Language: JavaScript`
* `With CSS Preprocessor: None`

Kurulumu tamamladık. Hadi gelin içeriği inceleyelim.

## Proje Root Dizini

![](<../.gitbook/assets/Screenshot 2023-05-07 at 20.35.47.png>)&#x20;

<mark style="color:blue;">Vue Fragment uygulaması</mark> config, public ve src klasörleri bize hazır olarak Jrontend paketi ile sunulmuştur. Config kısımları webpack module federation kullanarka Webpack configlerini içerir. Public kısımı index.html yer almaktadır. Src kısmında ise JavaScript dosyalarımızın ve geliştirmeleri bu kısımdan yaparak ilerleceğimiz kısımdır.

### Package.json İnceleyelim

```json
{
  "name": "vue_fragment",
  "version": "1.0.0",
  "scripts": {
    "start": "webpack serve --config config/webpack.dev.js",
    "build": "webpack --config config/webpack.prod.js"
  },
  "dependencies": {
    "vue": "^3.0.0"
  },
  "devDependencies": {
    "@babel/core": "^7.12.3",
    "@babel/plugin-transform-runtime": "^7.12.1",
    "@babel/preset-env": "^7.12.1",
    "@vue/compiler-sfc": "^3.0.2",
    "babel-loader": "^8.1.0",
    "css-loader": "^5.0.0",
    "file-loader": "^6.2.0",
    "html-webpack-plugin": "^4.5.0",
    "style-loader": "^2.0.0",
    "vue-loader": "^16.0.0-beta.9",
    "vue-style-loader": "^4.1.2",
    "webpack": "^5.4.0",
    "webpack-cli": "^4.1.0",
    "webpack-dev-server": "^3.11.0",
    "webpack-merge": "^5.2.0"
  }
}

```

Gerekli bağıntılarımızı(dependency) hali hazırda görüyoruz.&#x20;

`npm install` ile gerekli bağıntılarımızı yükleyelim

`npm start` komutu ile uygulamamızı ayağa kaldıralım.

Sorunsuz bir şekilde projemiz ayağa kalktı ise karşılaşmamız gereken ekranı aşağıdaki gibi olmalıdır.

<figure><img src="../.gitbook/assets/Screenshot 2023-05-07 at 20.36.46.png" alt=""><figcaption></figcaption></figure>
