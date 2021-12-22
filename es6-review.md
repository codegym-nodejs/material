# Destructing assignment 
  Là 1 cú pháp của es6 để lấy dữ liệu từ object hoặc array và gán nó vào các biến thông thường
  ### Sử dụng với array 
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
