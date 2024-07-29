# 🚀 SSH Guide

## 🌟 Definition

SSH or secure shell protocol
well http/https is a protocol to access a server
SSH is a protocol to access a computer
as we know shell is our tool to manipulate our computer(our OS)
so SSH is our tool to manipulate our computer remotely

![alt text](image.png)

## 🌟 First command to know

```sh
ssh {user}@{host} => shh root@162.52.125.65
```
## 🛠️ Why Use It

- 🛡️ To access GitHub repositories remotely.
- 💻 To access a computer remotely.
- 🌐 To access a deployment server remotely.


## 🔐 How SSH Works

In this section, we'll discuss the encryption techniques used in SSH to ensure secure communication.

### Symmetrical Encryption

Symmetrical encryption uses the same key to encrypt and decrypt messages between the host and the client. 

Do you know the Alice and Bob story? If not, here's a brief reminder:

> "Alice and Bob share a secret key. Alice encrypts her message with the key, and Bob decrypts it using the same key."

The algorithm used for this key exchange is called the Key Exchange Algorithm.

### Asymmetrical Encryption

Asymmetrical encryption uses a pair of keys: a public key and a private key. 

Here's another story about Alice and Bob:

> "Alice sends Bob her public key. Bob encrypts his message with Alice's public key. Only Alice can decrypt it with her private key."

The algorithm used for this process is the Diffie-Hellman Key Exchange Algorithm.

### Hashing

Now that we know how to exchange messages securely, we need to ensure that the messages aren't tampered with during transmission. This is where hashing comes in.

Hashing ensures data integrity by transforming the data into a fixed-size string of characters, which is unique to the original data. If the data is altered, the hash value will change, indicating tampering.

> "Hashing ensures that if someone tries to intercept and alter the message, it will be detected."

From now on, we have a secure remote connection.

![Secure Connection](image-2.png)



## 🛠️ Let's Use SSH with GitHub 🛠️

Here's a step-by-step guide to setting up SSH with GitHub:

### Step 1: Generate an SSH Key 🔑

Open your terminal and run the following command to generate a new SSH key:

```sh
ssh-keygen -t rsa -b 4096 -C "add something here"
```
Follow the prompts to save the key and set a passphrase if desired.

### Step 2: Copy the SSH Key 📋
```sh
cat ~/.ssh/id_rsa.pub
```
Select and copy the entire key output.

### Step 3: Add the Key to GitHub 🔧

1. Go to GitHub and log in to your account.
2. Navigate to **Settings** (click on your profile picture in the top right corner and select "Settings").
3. Click on **SSH and GPG keys** in the sidebar.
4. Click on **New SSH key**.
5. Paste your copied key into the "Key" field.
6. Give it a descriptive title and click **Add SSH key**.

### Step 4: Clone and Push 🎉

 Now you're all set! You can clone a repository using SSH  🎉

