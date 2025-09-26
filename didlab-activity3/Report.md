# Report for activity 3
Down below you can see the output of the scripts after being run
<img width="777" height="350" alt="image" src="https://github.com/user-attachments/assets/10790e24-5d35-4b42-b8b6-6868f73dead4" />
<img width="775" height="447" alt="image" src="https://github.com/user-attachments/assets/cbf7140a-8941-49d6-a148-3f21485a5f9e" />
<img width="779" height="486" alt="image" src="https://github.com/user-attachments/assets/8c5b26c0-29dc-4c3f-88b8-bfbfbcd28855" />
<img width="768" height="579" alt="image" src="https://github.com/user-attachments/assets/6b919a87-4193-4586-8fb0-c77fa5f9b3bf" />
<img width="522" height="144" alt="image" src="https://github.com/user-attachments/assets/e1603acf-6cc0-48eb-91a9-59c0834e389d" />


## Sreenshots of MetaMask
<img width="939" height="915" alt="image" src="https://github.com/user-attachments/assets/5327c4cf-6759-4452-a3ba-c2e503885a0a" />
<img width="921" height="618" alt="image" src="https://github.com/user-attachments/assets/0fda33ed-c081-4779-8592-75fedc63a74c" />
<img width="496" height="586" alt="image" src="https://github.com/user-attachments/assets/c85ccd2d-5335-47cf-ae5c-793d088c148f" />
<img width="664" height="840" alt="image" src="https://github.com/user-attachments/assets/dc98287d-67df-4e47-9991-bda1728a3d0e" />


## Console Output from airdrop.td
<img width="765" height="216" alt="image" src="https://github.com/user-attachments/assets/67a578a3-7f17-4d77-b495-642e2dcec0e1" />
The airdrop saves ~40% gas compared to naive transfers because of several Solidity design choices:
1. Custom Errors
Instead of require("string message"), the contract uses custom errors. These avoid embedding long revert strings in the bytecode, reducing deployment and runtime gas costs.
2. Calldata Usage
Function arguments (like recipient arrays) are marked as calldata, not memory. This avoids copying data into memory, which is more expensive, and allows cheaper direct reads.
3. Unchecked Loops
Loops that cannot overflow safely use unchecked { i++ }. Removing redundant overflow checks on counters saves gas in every iteration.
4. Single Transaction Amortization
The contract batches multiple transfers in one transaction. This spreads the fixed transaction overhead (21000 gas + event costs) across many recipients, making the average cost per transfer much lower than sending each individually.
