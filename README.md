<img width="1917" height="1070" alt="Screenshot 2026-04-07 at 9 29 20 PM" src="https://github.com/user-attachments/assets/45353b91-2198-4562-ae0e-3c5e137994c8" />

🔹 Full Code Explanation
1. License Identifier
// SPDX-License-Identifier: MIT
This tells that your code is using the MIT license.
Required for publishing contracts (especially on Ethereum).
2. Solidity Version
pragma solidity ^0.8.0;
Specifies the compiler version.
^0.8.0 means:
👉 Use version 0.8.0 or higher, but not 0.9.0+
3. Contract Declaration
contract MyFirtContract {
Defines a smart contract named MyFirtContract.
Think of it like a class in Java/C++.
4. State Variables
string public hey;
uint256 public no;
These are state variables (stored on blockchain).
string public hey;
Stores text
public → automatically creates a getter function
uint256 public no;
Stores a number (unsigned integer)
👉 Because they are public, Solidity internally creates:
function hey() public view returns (string memory)
function no() public view returns (uint256)
5. Commented Constructor (Important)
// constructor(string memory _hey, uint _no){
//   hey = _hey;
//   no = _no;
// }
A constructor runs only once when contract is deployed.
If you used it:
👉 You would set initial values during deployment.
Example:
MyFirtContract("Hello", 10)
But currently ❌ it's commented → so no initial values.
6. Main Function
function addInfo(string memory _hey, uint _no) public {
    hey = _hey;
    no = _no;
}
🔍 Explanation:
function addInfo(...) public
Anyone can call this function
Parameters:
_hey → input string
_no → input number
memory
Temporary storage (used for function inputs)

<img width="1382" height="861" alt="Screenshot 2026-04-07 at 9 29 44 PM" src="https://github.com/user-attachments/assets/23695491-7618-4e30-893c-63450807c8d3" />


