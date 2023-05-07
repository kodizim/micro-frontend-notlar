---
description: Module Federation kullanarak yapcağımız proje yapısına göz atalım.
---

# 1⃣ Projemizi Tanıyalım

<figure><img src="../.gitbook/assets/Screenshot 2023-05-07 at 19.44.15.png" alt=""><figcaption></figcaption></figure>

Micro frontend uygulaması oluşturma sürecini 4 aşamada gerçekleştireceğiz. Bu süreçte Module Federation, Jrontend, React ve Vue teknolojilerini kullanacağız. Başlangıç olarak React tabanlı bir composer uygulaması oluşturacağız ve ardından hem React hem de Vue ile fragment uygulamaları geliştireceğiz. Son olarak, bu fragment uygulamalarını composer uygulamasında çağırarak kullanacağız.

1. React Composer Uygulamasını Kuralım: a. Yeni bir React projesi oluşturun:
   1. `npx @jrontends/core@latest`
   2. `App name: jrontend-fun`
   3. `Project Type: Client App`
   4. `Client Type: composer`
   5. `Client Name: react-composer`
   6. `Port: 3000`
   7. `Framework/Library: React`
   8. `With Language: JavaScript`
   9. `With CSS Preprocessor: None`
2. React Fragment Uygulamasını Kuralım:&#x20;
   1. `npx @jrontends/core@latest`
   2. `App name: jrontend-fun`
   3. `Project Type: Client App`
   4. `Client Type: fragment`
   5. `Client Name: react-fragment`
   6. `Port: 3001`
   7. `Framework/Library: React`
   8. `With Language: JavaScript`
   9. `With CSS Preprocessor: None`
3. Vue Fragment Uygulamasını Kuralım:&#x20;
   1. `npx @jrontends/core@latest`
   2. `App name: jrontend-fun`
   3. `Project Type: Client App`
   4. `Client Type: fragment`
   5. `Client Name: vue-fragment`
   6. `Port: 3002`
   7. `Framework/Library: Vue`
   8. `With Language: JavaScript`
   9. `With CSS Preprocessor: None`
4. Son Adım:&#x20;
   1. React ve Vue fragment uygulamalarını React Composer uygulamasında çağırarak kullanmak için yapılandırmaları güncelleyin.&#x20;
   2. Geliştirme sunucusunu başlatın: `npm start`&#x20;
   3. Tarayıcınızda uygulamayı görüntüleyin ve her iki fragment uygulamanın da başarıyla yüklendiğini doğrulayın.

Bu 4 aşamayı tamamladığınızda, Module Federation, Jrontend, React ve Vue kullanarak basit bir micro frontend uygulaması oluşturmuş olacaksınız. Bu yapı, daha karmaşık uygulamalar için de temel alınarak geliştirilebilir.
