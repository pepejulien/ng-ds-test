# ng-ds-test

1. Name and describe the two main operations of a stack (to add and remove data).
   *In stack we use push to add data because we want to put at the end
   *To remove data we use pop because we want to remove the data at the, the last thing we put is goint to be the first one to     be remove.
   
2. Name and describe the two main operations of a queue (to add and remove data).
   *In queue we use enqueue tu put data
   *And also to remove data we use dequeue, but in this case the data to be remove will be the first data we added.
   
3.  Draw the tree resulting from adding the following sequence of numbers to an empty tree: 30, 45, 15, 10, 50, 40, 20, 27                                

                                  30
                    
                          
                      15                      45
                                                
                    
                10          20          40             50
                          
                          
                               27
                               
                               
4.  Is this tree balanced? If not, which rotation needs to be done? (Use the following rotation as an example: rightRotation(30), or leftRotation(10))
  
    Yes is balanced and it is not necesary to use a rotation
   
5.  Now add 29. Is the tree balanced? If not, which rotation needs to be done? (Use the following rotation as an example: rightRotation(30), or leftRotation(10))



                                  30
                    
                          
                      15                      45                            we have to use leftRotation(27)
                                                
                                                                              result:       27
                10          20          40             50
                                                                                        20       29
                          
                               27
                               
                                   29
                               
6.  Consider the following tree:
------5
---2-----8
-1--3
0
Now add 0 to the tree. Which one is the first node to go out of balance?
      R/ the node out of balance is 5.
      
7.  How do you fix this node? (Use the following rotation as an example: rightRotation(30), or leftRotation(10)) 
    I fix this using rightRotation(2)
    
8.  Divide  Conquer Combine Return

9.  12:00:00 hades				      trying to log in
    12:00:00 ares				        trying to log in
    12:00:00 zeus				        trying to log in
    12:00:00 buzz light year		trying to log in
    12:00:01  hades				            already log-in
    12:00:02 Kanye west			    trying to log in
    12:00:02 ares				              already log-in
    12:00:03 Taylor swift			trying to log in
    12:00:03 darkwing duck		trying to log in
    12:00:03 zeus				                already log-in
    12:00:04 Evil Mickey			trying to log in
    12:00:04 buzz light year		        already log-in
    12:00:05 Kaye west			            already log-in
    12:00:06 Taylor swift			          already log-in

10.  
process.stdin.resume(); 
process.stdin.setEncoding('ascii'); 
var input_stdin = ""; 
var input_stdin_array = ""; 
var input_currentline = 0; 

process.stdin.on('data', function (data) {
    input_stdin += data; 
}); 
process.stdin.on('end', function () {
    input_stdin_array = input_stdin.split("\n"); 
    main(); 
}); 
function readLine() { 
    return input_stdin_array[input_currentline++]; 
} 
/////////////// ignore above this line //////////////////// 
function main() { 
    var a0_temp = readLine().split(' '); 
    var a0 = parseInt(a0_temp[0]); 
    var a1 = parseInt(a0_temp[1]); 
    var a2 = parseInt(a0_temp[2]); 
    var b0_temp = readLine().split(' '); 
    var b0 = parseInt(b0_temp[0]); 
    var b1 = parseInt(b0_temp[1]); 
    var b2 = parseInt(b0_temp[2]); 
    
    var alice = 0; 
    var bob = 0; 
    if (a0 > b0) { 
        alice +=1; 
    } else if (a0 < b0) {
        bob +=1; 
    } 
    if (a1 > b1) {
        alice +=1; 
    } else if (a1 < b1) {
        bob +=1;
    } 
    if (a2 > b2) { 
        alice +=1; 
    } else if (a2 < b2) { 
        bob +=1; 
    } console.log(`${alice} ${bob}`); 
}

11.

process.stdin.resume();
process.stdin.setEncoding("ascii");
 
let _input = "";
process.stdin.on("data", input => _input += input);
process.stdin.on("end", () => res(_input));


/////////////// ignore above this line ////////////////////

const res = input => {
    const numbers = input.split(" ").map(i => parseInt(i));
    numbers.sort((a, b) => a - b)
    let minSum = 0;
    let maxSum = 0;
    for(let i = 0; i < numbers.length - 1; i++) {
        minSum += numbers[i];
        maxSum += numbers[i + 1];
    }
    console.log(minSum, maxSum);
};
