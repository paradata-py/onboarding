# Parada Hyperledger Blockchain Onboarding Guide

This guide will walk you through the steps required to connect to the Parada Hyperledger blockchain using Yarn, Node.js, NPX, and Hardhat on macOS, Linux, and Windows platforms.

## Prerequisites

Before you begin, ensure you have the following prerequisites installed on your system:

- Git (for cloning the repository)
- Node.js (v12.x or higher)
- Yarn package manager

### Step 1: Install Node.js

For macOS:

- Install Homebrew by running the following command in the Terminal:

  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

- Install Node.js using Homebrew:

 ```bash
 brew install node
  ```

For Linux (Ubuntu/Debian):
- Update your package index:
 ```bash
sudo apt update
sudo apt install nodejs
sudo apt install npm
  ```

For Windows:

- Download and install Node.js from the [Node.js official website](https://nodejs.org/).

### Step 2: Install Yarn

- To install Yarn globally, execute the following command:

```bash
npm install --global yarn
```

### Step 3: Install Hardhat
- Use Yarn to install Hardhat:
```bash
yarn add hardhat
```

### Step 4: Setting Up Your Project

- Start by creating a directory for your new project and then navigate into it:

```bash
mkdir my-parada-project && cd my-parada-project
```

- Initialize a new npm project:
```bash
npm init -y
```

- Next, install Hardhat in your project:
```bash
yarn add --dev hardhat
```

### Step 5: Initialize Hardhat
- Initialize a Hardhat project by running:

```bash
npx hardhat
```

### Step 6: Configure Hardhat
- In the root of your project, create a file named hardhat.config.js.
- Configure this file to connect to the Parada Hyperledger blockchain:
  
```javascript
module.exports = {
  networks: {
    parada: {
      url: "http://181.126.80.193",
      chainId: 1217
    }
  },
};
```

### Step 7: Verifying the Setup

- To ensure everything is set up correctly, compile your smart contracts with the following command:

```bash
npx hardhat compile
```

Successfully compiling your contracts indicates that your environment is correctly configured for the Parada Hyperledger blockchain.


