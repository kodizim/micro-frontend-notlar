# 3⃣ React Fragment Projesini Oluşturalım

Oluşturacak olduğumuz React Fragment Projesi bütün parçalarının birleştiği uygulama olacak.

Kurulum için proje adını **jrontend-fun** tercih etmiştik. Tekrar o projeye ekleme yapcağımız için aynı adı yazıyoruz.

* `npx @jrontends/core@latest`
* `App name: jrontend-fun`
* `Project Type: Client App`
* `Client Type: fragment`
* `Client Name: react_fragment`
* `Port: 3001`
* `Framework/Library: React`
* `With Language: JavaScript`
* `With CSS Preprocessor: None`

Kurulumu tamamladık. Hadi gelin içeriği inceleyelim.

## Proje Root Dizini

<img src="../.gitbook/assets/Screenshot 2023-05-07 at 20.25.38.png" alt="" data-size="original">&#x20;

<mark style="color:blue;">React Fragment uygulaması</mark> config, public ve src klasörleri bize hazır olarak Jrontend paketi ile sunulmuştur. Config kısımları webpack module federation kullanarka Webpack configlerini içerir. Public kısımı index.html yer almaktadır. Src kısmında ise JavaScript dosyalarımızın ve geliştirmeleri bu kısımdan yaparak ilerleceğimiz kısımdır.

### Package.json İnceleyelim

```json
{
  "name": "react_fragment",
  "version": "1.0.0",
  "scripts": {
    "start": "webpack serve --config config/webpack.dev.js",
    "build": "webpack --config config/webpack.prod.js"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-router-dom": "^5.1.2"
  },
  "devDependencies": {
    "@babel/core": "^7.12.3",
    "@babel/plugin-transform-runtime": "^7.12.1",
    "@babel/preset-env": "^7.12.1",
    "@babel/preset-react": "^7.12.1",
    "babel-loader": "^8.1.0",
    "clean-webpack-plugin": "^3.0.0",
    "css-loader": "^5.0.0",
    "html-webpack-plugin": "^4.5.0",
    "style-loader": "^2.0.0",
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

<figure><img src="../.gitbook/assets/Screenshot 2023-05-07 at 20.34.29.png" alt=""><figcaption></figcaption></figure>
