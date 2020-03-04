# How to prove my identity ?
As we all know, the internet is a complicated place. **No** texts that transmitted to you from the other end of the Internet can be guaranteed where they actually come from. And as an ordinary person, *Zcp* of course could not prove that all the texts are indeed from his **free will** either. Viruses, hackers, pressure from outside forces...are also likely to post information on his behalf.  
<br><br>

To solve this problem, **I announce** here, 
<br><br>
From now on(**2020.03.04**)，I'll sign **all** the texts in order to:  
1. Defend my rights to speak on the Internet;
2. Protect myself from being imitated by other people;
3. Provide a verification to the world that whether the messages are written by myself, whether the texts are consistent with my free will.

# GPG signature
I'll sign every file using my **PGP private key**, and share **the only trustable PGP public key** of mine here.(This README file will also be singed by me)

## Zcp's public key
- The *Fingerprint* is :`77F37C33368AD0B5D52810D1BF5738A17E62F3FC`  
- Public Key
[Zcp's PGP keys](./Zcp_PGP.pub)

**Notice that I haven't and will not upload my PGP keys to any key server, so if you found my PGP keys on any other places, it must be done by other people**

## Usage

### Sign
```bash
# Example: sign README.md
# Output signature file: sig.gpg
# --detach-sign: This option is the most useful for simply ensuring the integrity (but not privacy) of a large file
gpg --detach-sign -o sig.gpg README.md
```

### Verify
```bash
# Order matters, put signature file first!
gpg --verify sig.gpg README.md
```
If you haven't **import my PGP public key**, then the output will be(Chinese Version):
```
gpg: 签名建立于 2020年03月04日 星期x xx时xx分xx秒 JST
gpg:               使用 RSA 密钥 xxxx
gpg: 无法检查签名：No public key
```

### Import My Public Key
Download the `*.pub` [file](./Zcp_PGP.pub) directly.
Then run:
```bash
gpg --import Zcp_PGP.pub
```
And now you can verify this `README.md` file correctly.
**If this file is from me and haven't be edited, imitated by others**, the output of verification should be:

```
gpg: 完好的签名，来自于 xxxx
gpg: 警告：此密钥未被受信任签名认证！
gpg:       没有证据表明此签名属于其声称的所有者。
主密钥指纹： xxxx
    子密钥指纹： xxxx
```
The warning is because this public isn't trusted by default, you can trust it by:
```bash
gpg --edit-key [ID]
#gpg>
trust
```
Or, an example of verification **failure** :

```
gpg:               使用 RSA 密钥 xxxx
gpg: 已损坏的签名，来自于 xxxx
```



# I promise
- I will use the strictest methods to ensure I'm the **only** holder of my private keys.
- For statements that meet one of the following conditions, I will **only** publish them by digital signature:
    1. Make any statement about personal freedom, physical condition or mental condition;
    2. Declaration of withdrawal of certain statements made by myself;
    3. Other things that can be related to personal dignity or reputation.

If statements that belong to the above but are **not digitally signed**, or that such signatures cannot be verified, are **invalid**.
