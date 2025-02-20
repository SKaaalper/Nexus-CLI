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

7. Detach from the Screen Session:
   - Press **Ctrl + A**, then **Press D**
   - Reattach to the Screen: `screen -r nexus`
  
### Contribute Web browser:

1. Visit: https://app.nexus.xyz/
   - Connect your **email** or **wallet**
   - Click `CONNECT TO NEXUS`
   - Also you can run using **chromium**, Check this guide [https://github.com/0xmoei](https://github.com/0xmoei/Install-Chromium-Linux-Browser)

  ![image](https://github.com/user-attachments/assets/09942e02-33e6-497b-bae1-1544a6532865)






   

     
