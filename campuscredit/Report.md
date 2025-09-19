In this repo, I completed activity 2 for my blockchain class. 
## Overview
I started by checking the required versions of Node and npm. Then, I initialized the Hardhat project by creating a JavaScript project and installing the necessary dependencies. I configured Hardhat to support EIP-1559, enabling meaningful base fees and priority tips on the local chain to facilitate fee analysis.

Next, I wrote the ERC-20 token contract with an initialSupply value. In a separate terminal, I started a local Hardhat node, which provided 20 funded test accounts. In another terminal, I deployed the contract to the local network, which returned the contract address.

After that, I ran interaction scripts—transferring tokens, setting approvals, and experimenting with different tips—which produced three transaction hashes and their corresponding block information. The final step involved analyzing transaction receipts, blocks, EIP-1559 fields, and even decoding data for further insights.

### Hardhat Compiling
<img width="710" height="177" alt="image" src="https://github.com/user-attachments/assets/0f430dc1-e973-48ae-b5f7-d265a5daeedd" />

### Deploy Script
<img width="575" height="156" alt="image" src="https://github.com/user-attachments/assets/855bc669-b1a0-4b24-a5ee-3ceee3892574" />

### Interact Script
<img width="647" height="282" alt="image" src="https://github.com/user-attachments/assets/c9fbdbc1-7d38-4a67-8356-eba6f80d91b7" />

### Analyze Script
<img width="770" height="733" alt="image" src="https://github.com/user-attachments/assets/ccae8be0-1bb7-4aca-8680-a302da0e5c8e" />
<img width="772" height="382" alt="image" src="https://github.com/user-attachments/assets/99a7a3a1-e883-4bba-9148-cc6d00ac3ce1" />
