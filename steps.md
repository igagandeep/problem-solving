Solution 1:

function steps(n) {
  for(let row = 0; row < n; row++){
    let stair = "";

    for(let col = 0; col < n;col++){
      if(col <= row){
        stair += "#";
      }
      else{
        stair += " ";
      }
    }
    console.log(stair);
}

}



SOlut2:


function steps(n, row = 0, stair = '') {
    if(n === row){
      return;
    }

    if(n === stair.length){
      console.log(stair);
      return steps(n, row + 1);
    }

    const add = stair.length <= row ? '#' :  ' '
    steps(n, row, stair + add);
}
