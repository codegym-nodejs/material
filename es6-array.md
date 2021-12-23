# Array Method trong es6
  1. forEach
    const array1 = ['a', 'b', 'c'];
    array1.forEach(element => console.log(element));

  2. reduce
    Vd: Tính trung bình của các phần tử trong array
    const array1 = [1, 2, 3, 4];
    let average = array1.reduce((preValue, curValue, index, array) => {
      preValue += curValue;
        if(index === array1.length - 1) {
        return preValue / array1.length;
        }
        else {
        return preValue
        }
    });
    console.log(average);

    Vd : Đếm số lần xuất hiện của các phần tử trong mảng:

    const array1 = [1, 2, 3, 4, 4];
    let count = array1.reduce((preValue, curValue) => {
      
      preValue[curValue] = (preValue[curValue] || 0 ) + 1;
      
      console.log(preValue[curValue]);
        return preValue;
    }, {});
    console.log(count);