solution 1:

function pyramid(n) {
    const midpoint = Math.floor((2 * n -1) / 2);
    
    for(let row = 0; row < n; row++){
        let level = '';
        
        for(let col = 0; col < 2 * n -1; col++){
            if(midpoint-row <= col && midpoint + row >= col){
                level += "#"
            }
            else{
                level += " "
            }
        
            
        }
        console.log(level);
        
    }    
}


Solution 2: 


function pyramid(n, row = 0, level = '') {
    
    if(row === n)return;
    
    
    const midpoint = Math.floor((2 * n -1) / 2);
    
    
    if(level.length === (2 * n -1)){
        console.log(level);
        return pyramid(n, row + 1);
    }
    
    const add = midpoint - row <= level.length && midpoint + row >= level.length ? '#' : ' ';
    pyramid(n, row, level + add);

}
