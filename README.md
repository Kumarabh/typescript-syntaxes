####                                  type object
 type User = {
     firstName: string,
     lastName: string,
     email?: string,
     contact?: number
 }

 let user1: User = {
     firstName: 'John',
     lastName: 'Doe'
 }
 console.log(`${user1}`)

####                                  Array of numbers
 const data3: Array<number | string> = [1, 2, 3, 'A'];
 const arr2: (number | string)[] = [1, 2, 3, 'A'];
 const arr3: number[] | string[] = [1, 2, 3];


####                                  Tuples
 let user: [number, string];
 user = [1, 'Abhishek'];
 console.log(user);

  type User = [number, string];
  const user1: User = [1, 'John Doe'];
  console.log(user1);


####                                  enum type
 enum SeatChoice {
     ASILE = 'aisle',
     MIDDLE = 'middle',
     WINDOW = 'window'
 }

 const hcSeat = SeatChoice.ASILE;
 console.log(hcSeat)

####                                  interface type
 interface User {
     firstName: string,
     lastName: string,
     email?: string,
     contact?: string,
     getFullName: () => string,
     getEmail() : string | undefined
 }

 const user1: User = {
     firstName: 'John',
     lastName: 'Doe',
     email: 'John.doe2010@gmail.com',
     getFullName() {
         return this.firstName + ' ' + this.lastName
     },
     getEmail: function (): string | undefined {
         return this.email ? this.email : undefined
     }
 }

 console.log(user1.getFullName())
 console.log(user1.getEmail())

####                                   reopening interface (redeclaration of interface appending new type) 

 1.
 interface User {
     firstName: string,
     lastName: string
 }

 interface User {
     email: string
 }

 const user: User = {
     firstName: 'John',
     lastName: 'Doe',
     email: 'John.doe2010@gmail.com'
 }
 console.log(user);

####                                   inheritence
 interface User {
     firstName: string,
     lastName: string
 }

 interface Admin extends User {
     role: 'admin' | 'superadmin'
 }

 const user1: Admin = {
     firstName: 'John',
     lastName: 'Doe',
     role: 'admin'
 }
 console.log(user1)
 
 ----
 
 ### EXAMPLE 1
 
---------index.ts

import { Product } from "./types/dataTypes";

// const productCode: ProductCode = 101;
// const productName: ProductName = 'Product 01';

// console.log(productCode)
// console.log(productName);

const product: Product = {
  productCode: 11,
  productName: "Shoe",
  isAvailable: true,
  productDescription: "Adidas Shoe, Size-8",
  price: 2300.50,
  storeId: '900',
  getProductDetails(){
    return {
      productCode: this.productCode, 
      productName: this.productName, 
      isAvailable: this.isAvailable, 
      productDescription: this.productDescription, 
      price: this.price, 
      storeId: this.storeId
    } as Product
  }
}

console.log(product.getProductDetails());

 ---------dataTypes.ts
 
 // number
export type ProductCode = number;

// string
export type ProductName = string;

// boolean
export type IsAvailable = boolean;

//object
export type Product = {
    productCode: ProductCode,
    productName: ProductName,
    isAvailable: IsAvailable,
    productDescription: string,
    price: number,
    storeId: string,
    getProductDetails: () => Product
}




 
