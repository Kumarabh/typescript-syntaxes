// ---------------------------type object
// type User = {
//     firstName: string,
//     lastName: string,
//     email?: string,
//     contact?: number
// }

// let user1: User = {
//     firstName: 'John',
//     lastName: 'Doe'
// }
// console.log(`${user1}`)

// ---------------------------Array of numbers
// const data3: Array<number | string> = [1, 2, 3, 'A'];
// const arr2: (number | string)[] = [1, 2, 3, 'A'];
// const arr3: number[] | string[] = [1, 2, 3];


// ---------------------------Tuples
// let user: [number, string];
// user = [1, 'Abhishek'];
// console.log(user);

//  type User = [number, string];
//  const user1: User = [1, 'John Doe'];
//  console.log(user1);


// ---------------------------enum type
// enum SeatChoice {
//     ASILE = 'aisle',
//     MIDDLE = 'middle',
//     WINDOW = 'window'
// }

// const hcSeat = SeatChoice.ASILE;
// console.log(hcSeat)

// ---------------------------interface type
// interface User {
//     firstName: string,
//     lastName: string,
//     email?: string,
//     contact?: string,
//     getFullName: () => string,
//     getEmail() : string | undefined
// }

// const user1: User = {
//     firstName: 'John',
//     lastName: 'Doe',
//     email: 'John.doe2010@gmail.com',
//     getFullName() {
//         return this.firstName + ' ' + this.lastName
//     },
//     getEmail: function (): string | undefined {
//         return this.email ? this.email : undefined
//     }
// }

// console.log(user1.getFullName())
// console.log(user1.getEmail())

// --------------------------- reopening interface (redeclaration of interface appending new type) 

// 1.
// interface User {
//     firstName: string,
//     lastName: string
// }

// interface User {
//     email: string
// }

// const user: User = {
//     firstName: 'John',
//     lastName: 'Doe',
//     email: 'John.doe2010@gmail.com'
// }
// console.log(user);

// --------------------------- inheritence
// interface User {
//     firstName: string,
//     lastName: string
// }

// interface Admin extends User {
//     role: 'admin' | 'superadmin'
// }

// const user1: Admin = {
//     firstName: 'John',
//     lastName: 'Doe',
//     role: 'admin'
// }
// console.log(user1)

// ------------------------------ class
class User {
    firstName: string;
    lastName: string;

    constructor(firstName: string, lastName: string) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

const user1 = new User('Abhishek', 'Kumar');
console.log(user1);

