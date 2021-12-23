# Sở khai
  let Thinh = {
    name : 'Thinh', 
    age : 24,
  };

  let Nam = {
    name: 'Nam',
    age: 24
  }

# Es5 trở về trước không có Class
  function Person(_name, _age) {
    this.name = _name ;
    this.age = _age;
  }

  let thinh = new Person("Thinh", 24);
  let nam = new Person("Nam", 24);

## Kế thừ sử dụng prototype để kế thừa
  function Person(_name) {
    this.name = _name
  }

  Person.prototype.showName = function() {
    console.log(this.name);
  }

  function Male(_age) {
    this.age = _age;
  }

  Male.prototype = new Person();
  Male.prototype.showAge = function() {
    console.log(this.age);
  }

  let thinh = new Male(24);

# Từ ES 6 trở đi cú pháp khai báo class:

  class Classname {
    constructor(arg1, arg2){
    this.prop1 = arg1;
    this.prop2 = arg2;
    }
    getProp1 {
      return this.prop1;
    }
  }

  Ví dụ:
  
  class Person {
    constructor(_name, _age){
      this.name = _name;
      this.age = _age;
    }

    getName() {
      console.log(this.name);
    }
    getAge() {
      console.log(this.age)
    }
  }

  let thinh = new Person("Thinh", 24);

# Từ khóa static
  class Person {
    constructor(_name, _age){
      this.name = _name;
      this.age = _age;
    }

    static countPerson = 0;

    static increasePerson() {
      this.countPerson += 1;
    }

    getName() {
      console.log(this.name);
    }
    getAge() {
      console.log(this.age)
    }
  }

  Person2.countPerson;

# Setter, Getter trong ES 6 class;
  class Employee {
    constructor (name, age) {
        this.name = name;
        this.age = age;
    }
    set employeeName (name) {
        this.name = name;
    }
    get employeeName () {
        return this.name;
    }
    set employeeAge (age) {
        this.age = age;
    }
    get employeeAge () {
        return this.age;
    }
};

myEm.employeeName = "A";

# Kế thừa trong Es6 class

class Person {
  constructor(_name) {
    this.name = _name;
  }
  getName() {
    return this.name;
  }
}

class Male extends Person {
  constructor(_name, _age) {
    super(_name);
    this.age = _age;
  }
  getAge() {
    return this.age;
  }

  getName() {
    super.getName();
    console.log("this is child class");
  }
}

Muốn dùng method của class cha, dùng từ khóa super.methodName