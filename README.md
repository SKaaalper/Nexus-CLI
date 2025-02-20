# Nexus Testnet II CLI Installation

![image](https://github.com/user-attachments/assets/70443224-d737-4104-ba4f-3140102845eb)

Nexus Layer 1: Planetary scale, Exponential performance. Built for everyone.

### **Official Docs**: [https://docs.nexus.xyz/](https://docs.nexus.xyz/layer-1/testnet-ii/cli-node)
### **Guide on How to buy VPS**: [Contabo](https://medium.com/@Airdrop_Jheff/guide-on-how-to-buy-a-vps-server-from-contabo-and-set-it-up-on-termius-0928e0e5cb5d)

### NEX POINTS:

   - Earn NEX Points by contributing computing power and actively engaging with the Nexus ecosystem through various interactions and activities.
   - You can connect and manage multiple devices—including desktops, laptops, mobiles, and servers—under one Nexus account.
   - You can prove computations across multiple browser tabs at the same time.

### Create an Account:

   - Visit: [https://app.nexus.xyz](https://app.nexus.xyz)
   - If you were on Testnet 1 before, you can connect your email to earn more points soon.
   - Follow the account linking instructions.
   - Your contributions will earn `NEX` Points.
   - Track your progress on the leaderboard.
   - Manage all your nodes in one place.
  
### INSTALLATION:

1. Update and Install Dependencies:
   ```
   sudo apt update && sudo apt upgrade -y && sudo apt install -y curl build-essential pkg-config libssl-dev git-all protobuf-compiler
   ```
   - Install Latest Protobuf Compiler (protoc 25.2)
   ```
   PROTOC_VERSION=25.2
   wget https://github.com/protocolbuffers/protobuf/releases/download/v${PROTOC_VERSION}/protoc-${PROTOC_VERSION}-linux-x86_64.zip
   sudo unzip -o protoc-${PROTOC_VERSION}-linux-x86_64.zip -d /usr/local
   rm protoc-${PROTOC_VERSION}-linux-x86_64.zip
   sudo chmod +x /usr/local/bin/protoc
   ```
   ```
   protoc --version
   ```
   - Output: `libprotoc 25.2`


2. Install `Rust` and `Cargo`:
   ```
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```
   - Press `Enter` to Default

3. Configure Rust Environment:
   ```
   source $HOME/.cargo/env && echo 'source $HOME/.cargo/env' >> ~/.bashrc && source ~/.bashrc
   ```

4. Add the `riscv32i` Target:
   ```
   rustup target add riscv32i-unknown-none-elf
   ```

5. Create a `Screen` Session:
   ```
   screen -S nexus
   ```

6. Install `Nexus` CLI:
   ```
   curl https://cli.nexus.xyz/ | sh
   ```
   - Do you agree to the Nexus Beta Terms of Use (https://nexus.xyz/terms-of-use)? (Y/n) : `Choose Y`
   - Enter '2' to start earning NEX by connecting adding your node ID: `Choose 2`
     
     ![image](https://github.com/user-attachments/assets/d0295198-4818-4514-8ac1-de0c98f77e48)

   - Enter your `node ID`, You can get it on the website [HERE](https://app.nexus.xyz/nodes): Click **Add Node** > Click **Add CLI** > Copy the **Node ID** and paste it.
     
     ![image](https://github.com/user-attachments/assets/00b1bba0-e714-41f4-a173-d8215db80934)


   - If this is the result on your Prover node, then you're good. Now, you just need to wait for it to sync to your dashboard.

     ![image](https://github.com/user-attachments/assets/3620ed03-61dd-4602-946d-6c9949370a51)

### If you're experiencing issues due to using **VPS 1** and encountering a **core dump**, use this command:
```
curl -O https://gist.githubusercontent.com/NodeFarmer/013a495f61761903b1378a64cbe64810/raw/2524770f735e2c292d30e02c11f5447b052f63ad/nexus_swap.sh && chmod +x nexus_swap.sh && ./nexus_swap.sh
```

1. Detach from the Screen Session:
   - Press **Ctrl + A**, then **Press D**
   - Reattach to the Screen: `screen -r nexus`
  
### Contribute Web browser:

1. Visit: https://app.nexus.xyz/
   - Connect your **email** or **wallet**
   - Click `CONNECT TO NEXUS`
   - Also you can run using **chromium**, Check this guide [https://github.com/0xmoei](https://github.com/0xmoei/Install-Chromium-Linux-Browser)

  ![image](https://github.com/user-attachments/assets/09942e02-33e6-497b-bae1-1544a6532865)

2. Many are facing **auto-disconnect** issues. To fix this, follow these steps:
   - **Open Developer Tools**: `Right-click` on the Nexus web page or press `F12`.
   - **Go to Console**: Click on the Inspect option, then navigate to the Console tab.
   - **Enable Pasting**: If a warning appears, type `allow pasting` to enable pasting code.
   - **Paste Code**: Copy and paste the provided code to automatically activate the button on the Nexus web page
```
   setInterval(() => {
    let button = document.querySelector('.relative.w-24.h-16');

    if (button) {
        let isOff = button.classList.contains('border-gray-400');

        if (isOff) {
            button.click();
            console.log("Button turned ON!");
        }
    }
}, 1000);
```

![image](https://github.com/user-attachments/assets/95cfea78-e02b-452c-9e9b-d0faf4abddca)


**Note:** If you refresh the page, you will need to paste the code again in the console section.




   

     
