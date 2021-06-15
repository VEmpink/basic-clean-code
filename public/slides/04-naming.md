# Naming Conventions

- ### Gunakan penamaan yang bermakna

  **Bad**

  ```js
  // Data apa? Komentar, postingan, apa cuma data session aja?
  getUserData();

  // Info apa? Info tentang statistik pengguna apa cuma info user token aja?
  getUserInfo();
  ```

  **Good**

  ```js
  getUserPosts();
  ```

  **Also Good**

  ```js
  // Pakai penamaan yang lebih deskriptif aja daripada ringkas
  getUserPostsByEmail();
  getUserPostsByUserNameOrEmail();
  ```

  **More Descriptive but Bad**

  ```js
  getUserPostsFromDatabase();
  getUserPostsFromAPI();
  getUserPostsFromLocalStorage();
  ```

- ### Penamaan logical variable

  Gunakan `is` `has` `was` untuk menamai logical variable.

  **Bad**

  ```js
  const token = getUserToken();

  if (token) {
    redirect('/dashboard');
  }
  ```

  **Good**

  ```js
  const userHasToken = getUserToken();

  if (userHasToken) {
    redirect('/dashboard');
  }
  ```

  **Also Good**

  ```js
  import isEmpty from 'lodash/isEmpty';

  const token = getUserToken();

  if (!isEmpty(token)) {
    redirect('/dashboard');
  }
  ```

- ### Hindari satu huruf nama variable

  **Bad**

  ```js
  const d = new Date();
  ```

  **Good**

  ```js
  const currentDate = new Date();
  ```

- ### Hindari penamaan variable menggunakan underscores

  **Bad**

  ```js
  const _date = new Date();
  const current_date = new Date();
  ```

  **Good**

  ```js
  const currentDate = new Date();
  ```

- ### Hindari menggunakan konteks yang tidak dibutuhkan

  **Bad**

  ```
  const fighterJet = {
    jetType: 'A-10 Warthog',
    jetColor: 'Gray',
    jetMainGunType: 'GAU-8 Avenger 30mm',
  };

  function replaceJetMainGun(jet) {
    jet.jetMainGunType = 'M61 20mm';
  }
  ```

  **Good**

  ```
  const fighterJet = {
    type: 'A-10 Warthog',
    color: 'Gray',
    mainGunType: 'GAU-8 Avenger 30mm',
  };

  function replaceJetMainGun(jet) {
    jet.mainGunType = 'M61 20mm';
  }
  ```
