# Lainnya

- ### Hindari kondisional negatif

  **Bad**

  ```js
  if (!isNotEmpty(value)) {
  }
  ```

  **Good**

  ```js
  if (!isEmpty(value)) {
  }
  ```

- ### Disarankan menggunakan lebar 80 karakter untuk setiap baris kode
- ### Disarankan menggunakan lebar space untuk sebuah tab hanya antara 2 dan 4 space
- ### Hindari menggunakan double quote untuk sebuah string di Javascript
- ### Hindari menggunakan `else` pada sebuah if-statement
- ### Biasakan untuk memberikan garis baru untuk setiap pembuka/penutup multi-line if-statement
- ### Hindari menggunakan nested ternary operator
- ### Hindari menggunakan `var` untuk mendeklarasikan sebuah variable
- ### Disarankan untuk mengurutkan deklarasi `const` -> `let`
- ### Biasakan untuk memberikan satu garis baru untuk setiap penutupan brackets
- ### Biasakan untuk memisahkan `return` statement dengan satu garis baru
- ### Disarankan untuk selalu menerapkan code spliting
- ### Biasakan untuk menghapus code yang tidak digunakkan
- ### Komentari sebuah kode seperlunya
- ### Disarankan kalau mengimport module itu seperlunya

- ### Terapkan urutan kode React dari `props` -> `useContext` -> `useReducer` -> `useState` -> `useRef` -> `useMemo` -> `useCallback` -> `useImperativeHandle` -> `useEffect/useDebugValue/useLayoutEffect` -> `return`
