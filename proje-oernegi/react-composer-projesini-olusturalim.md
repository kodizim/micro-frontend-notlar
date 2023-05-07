# 2⃣ React Composer Projesini Oluşturalım

Oluşturacak olduğumuz React Composer Projesi bütün parçalarının birleştiği uygulama olacak. İlk adım olarak Jrontend paketini kullanarak kurulumu yapıp son adımda tekrar bu projeye geri döneceğiz.



Kurulum için proje adını **jrontend-fun** tercih ediyorum.

* `npx @jrontends/core@latest`
* `App name: jrontend-fun`
* `Project Type: Client App`
* `Client Type: composer`
* `Client Name: react-composer`
* `Port: 3000`
* `Framework/Library: React`
* `With Language: JavaScript`
* `With CSS Preprocessor: None`

Kurulumu tamamladık. Hadi gelin içeriği inceleyelim.

## Proje Root Dizini

![](<../.gitbook/assets/Screenshot 2023-05-07 at 20.15.29.png>)

<mark style="color:blue;">React Composer uygulaması</mark> config, public ve src klasörleri bize hazır olarak Jrontend paketi ile sunulmuştur. Config kısımları webpack module federation kullanarka Webpack configlerini içerir. Public kısımı index.html yer almaktadır. Src kısmında ise JavaScript dosyalarımızın ve geliştirmeleri bu kısımdan yaparak ilerleceğimiz kısımdır.

### Package.json İnceleyelim

```json
{
  "name": "react-composer",
  "version": "1.0.0",
  "scripts": {
      "start": "webpack serve --config config/webpack.dev.js",
      "build": "webpack --config config/webpack.prod.js"
  },
  "dependencies": {
    "react": "^17.0.1",
    "react-dom": "^17.0.1",
    "react-router-dom": "^5.2.0"
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

![](<../.gitbook/assets/Screenshot 2023-05-07 at 20.22.30.png>)
