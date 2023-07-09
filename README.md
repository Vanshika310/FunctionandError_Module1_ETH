# FunctionandError_Module1_ETH

This solidity program returns the sum as an output of two numbers that will be given as input by the user. This code will use error handling statements such as require(), assert(), and revert(). This syntax is simple to understand. This code is written to give a brief explanation of the error-handling statements. 

# Description

This is the simple code that uses solidity programming. Solidity, a programming language for creating smart contracts for the Ethereum network, this program is a straightforward contract. The program contains a function along with two parameters and an unsigned integer type output which will return the parameter's sum. It also contains the if condition for the revert statement. 

# Getting Start

To get started with this programming type, you should first open up the solidity compiler that is Remix online IDE: https://remix.ethereum.org/. Now, when the IDE opens you first have to create a file in which you can write the code, so first click on the new file which is given at the left-hand sidebar. Name the file of your wish and save the file with an extension .sol. For example, sum.sol. Now, write the given code in

    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.0;
    
    contract addNumbers{
        function Sum(uint a, uint b) external pure returns(uint){
            require(a > 0, "First Input must be greater than 0");
            require(b > 0, "The second input must also be greater than 0");
            
            uint result = a + b;
    
            assert(result >= a && result >= b);
    
            if(result < a || result < b){
                revert("Error occurred somewhere");
            }
    
            return result;
    
        }
    }

# Explanation

Here, in the smart contract called "addNumbers", I have a function called "Sum" which is taking two unsigned integers a and b as input and return their sum as an output.

Now, the first statement require() is used. This statement is used to check whether the input meets certain conditions or not. In this case, it is required for both a and b to be greater than 0 otherwise the function execution will stop and revert with an error message displayed above in the code.

In this next step, the result is declared as an unsigned integer which is returning the sum of two inputs. 

Next, we have the assert() statement. This statement is used to verify the conditions that must always be true. Here, in this code, it is needed that the result should be greater than or equal to both a and b or else it will return an internal error.

Lastly, we have the revert() condition. This statement will explicitly return the condition and provide an error message. Here, if the result is less than a or b then the revert() will give an error and says that the error occurred somewhere.  

In the end, it will return the result.

# Compilation

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.8", and then click on the "Compile sum.sol" button.

Once the code is compiled, you can deploy the contract. When you deploy the contract you will see the addNumber. Below that, you have to provide the values for a and b. If you provide the values according to the conditions then it will simply give you the result. Otherwise, the error will be shown up.

# License

This project is licensed under the MIT License - see the LICENSE.md file for details













                                                
