class Product {
  constructor(name, price) {
    this.name = name;
    this._price = price;
  }

  get price() {
    return this._price;
  }

  set price(value) {
    if (value < 0) {
      console.log("No negative prices!");
    } else {
      this._price = value;
    }
  }
}


const pen = new Product("Pen", 25);
pen.price = -10;
console.log(pen.price);
