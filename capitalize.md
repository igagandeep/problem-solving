Answer 1
function capitalize(str) {

    const words = [];
    
    for(let ele of str.split(" ")){
    
        words.push(ele[0].toUpperCase() + ele.slice(1))
        
    }
    
    return words.join(" ");
}


Answer 2



function capitalize(str) {

    let result = str[0].toUpperCase();
    
   for(let i = 1; i < str.length; i++){
   
      if(str[i - 1] === " "){
      
        result += str[i].toUpperCase();
        
      }
      
      else{
      
      result += str[i]
      
      }
      
   }
   
console.log(result)
   return result;
}
