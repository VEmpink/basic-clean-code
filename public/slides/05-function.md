# Function Conventions

- ### Hindari menggunakan fungsi `eval()`
- ### Idealnya fungsi hanya memiliki maksimal 2 parameter

  **Bad**

  ```
  function generateCoordinate(city, street, zipCode) {}
  ```

  **Good**

  ```
  function generateCoordinate(address) {
    const { city, street, zipCode } = address;
  }
  ```

- ### Biasakan untuk memberikan default value pada sebuah parameter function
- ### Hindari penulisan fungsi global

  **Bad**

  ```
  Array.prototype.diff = function diff(comparisonArray) {
    const hash = new Set(comparisonArray);
    return this.filter((elem) => !hash.has(elem));
  };
  ```

  **Good**

  ```
  class SuperArray extends Array {
    diff(comparisonArray) {
      const hash = new Set(comparisonArray);
      return this.filter((elem) => !hash.has(elem));
    }
  }
  ```
