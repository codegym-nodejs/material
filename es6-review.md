# Destructing assignment 
  Là 1 cú pháp của es6 để lấy dữ liệu từ object hoặc array và gán nó vào các biến thông thường
  # Sử dụng với array 
      let [firstName, lastName] = ["LeVan", "Thinh"]
  
    tương đương với cú pháp:
	
      let firstName, lastName;
      let userInfo = res.data;
      firstName = userInfo[0], lastName = userInfo[1];

  ### Khai báo giá trị default
      let [firstName, lastName="Thinh"] = ["Le Van"]

  ### Bỏ qua một số phần tử
      let [ a, , b] = [“AA”, “BB”, “CC”]
    
  ### Gán các giá trị còn lại của mảng cho 1 biến

      let [a,b, …others] = [1,2,3,4,5,6,7,8,9]

  ### Sao chép mảng:

      let a = [1,2];
      let […b] = a;

  # Sử dụng với object

    ### Cú pháp cơ bản
      let {firstName, lastName} = {firstName: "Le Van", lastName: "Thinh"} 

    ### Gán lại tên biến

      let {firstName: fName, lastName: lName} = {firstName: "Le Van", lastName: "Thinh"}

    Tương đương với cú pháp:

      let obj = {firstName: “Le Van”, lastName: “Thinh”} 
      let firstName = obj.firstName;
      let lastName : obj.lastName;

    ### Khai báo giá trị default
      let {firstName, lastName = “Thinh”} = {firstName: “Le Van”}

    ### Gán các giá trị còn lại của object cho một biến khác
      let {a, b, ...others} = {a:10, b : 20, c:30, d: 40};

    ### Sử dụng array và object lồng nhau

      let options = {
          size: {
              width: 300,
              height: 400,
          },
          items: [1,2],
      }

      let {size : {width: myWidth, height: myHeight}, items: myItems} = options

    ### Set các tham số default cho một hàm

      function myFnc( {x = 1, y = 2} = { } ){
        console.log(x,y);
      };

      myFnc();

# Spread Syntax
  ### 1. Sử dụng như rest parameters
    function Fnam(…args) {
	    // code here
    }

  ### 2. Clone array, object

    C1: sử dụng assign

      var obj = {
          id : 1,
          name: 'Thinh',
      }

      var clone = Object.assign({}, obj);

    C2: Spread Syntax

      let clone = {…obj};

      let cloneArray = […sourceArray];

  ### 3.	Merge array
    let arr1 = [1,2,3]
    let arr2 = [4,5,6]

    // C1: sử dụng hàm concat
    let arr1 = [1,2,3];
    let arr2 = [4,5,6];
    let arr3 = arr1.concat(arr2);

    // C2: sử dung spread syntax
    
    let arr4 = [...arr1, ...arr2];

  ### 4.	Merge properties của object
    let obj1= {
      id: 1,
      name: "mot",
      hi : "hello"
    };
    let obj2 = {
        id: 2,
        name: "hai"
    }

    let obj3 = {...obj1, ...obj2};


# Arrow function

  ### C1:
    function Name(parameters) {
      //code block
    }
  ### C2:
    let name = function(parameters) {
      //code block
    }

  ### C3:
    let functionName = (parameters) => {
      //code block
      return number % 2 === 0
    }

  let checkEvent = (number) =>  number % 2 === 0

  Vd : let min = (a,b) => (a < b ? a: b);


