---
description: Projemizin son adımlarını tamamlayalım 🎉
---

# 🎊 Projemizin Son Adımları

## React Composer Uygulaması

Uygulama dizinine gidip config/webpack.dev.js dosyasını açalım.

```javascript
const { merge } = require('webpack-merge')
const ModuleFederationPlugin = require('webpack/lib/container/ModuleFederationPlugin')
const commonConfig = require('./webpack.common')
const packageJson = require('../package.json')

const devConfig = {
    mode: 'development',
    devServer: {
        port: 3000,
        historyApiFallback: {
            index: 'index.html',
        },
    },
    plugins: [
        new ModuleFederationPlugin({
            name: 'react-composer',
            remotes: {
                react_fragment: 'react_fragment@http://localhost:3001/remoteEntry.js',
                vue_fragment: 'vue_fragment@http://localhost:3002/remoteEntry.js',
            },
            shared: packageJson.dependencies,
        }),
    ],
}

module.exports = merge(commonConfig, devConfig)

```

Şeklinde düzenleyelim. Oluşturmuş olduğumuz react-fragment ve vue-fragment uygulamalarımızı ekliyor ediyor gibi düşünebilirsiniz.



Src/App.js dosyamızı gidip eklemiş olduğumuz React fragment'ın Composer içinde çalışmasını sağlayalım.\


```jsx
import React, {lazy, Suspense} from 'react'

const ReactFragment = lazy(() => import('react_fragment/App'));

const App = () => {
    return (
        <div>
            <h1>Welcome react-composer</h1>
            <Suspense fallback={"Loading.."}>
                <ReactFragment/>
            </Suspense>
        </div>
    )
}

export default App
```

Ve son dokunuşu da yaptığımıza göre tekrardan bütün uygulamalarımızı npm start diyerek ayağa kaldıralım. Ayrı ayrı çalışan javascript projelerimizi tek bir kapsayıcı react-composer uygulamasında birleşmiş hali bizi aşağıdaki gibi karşılıcak.\
\


<figure><img src="../.gitbook/assets/Screenshot 2023-05-07 at 20.55.35.png" alt=""><figcaption></figcaption></figure>

### <mark style="color:red;background-color:orange;">İlk micro frontend uygulamamızı tamamlamış olduk.</mark>&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-05-07 at 20.55.59.png" alt=""><figcaption><p>:)</p></figcaption></figure>

_**NOT: Daha kapsamlı açıklamalar ve uygulamalar eklenecektir.**_&#x20;

_**Projenin GitHub linki:**_ [_**https://github.com/fport/jrontend-fun**_](https://github.com/fport/jrontend-fun)
