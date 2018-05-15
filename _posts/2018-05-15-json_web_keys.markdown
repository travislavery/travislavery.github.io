---
layout: post
title:      "JSON Web Keys"
date:       2018-05-15 23:41:20 +0000
permalink:  json_web_keys
---


So, here we are, all excited to be learning about the wonders of security in an online world. Today, I’ll be doing a brief overview of what a JWK (json web key) is, and what purpose it serves.

Whenever you want to use a public-key cryptosystem, you use whoever it is that you are sending an encrypted message to’s public key to turn plain-text (unencrypted data) into cipher-text (encrypted data). The recipient is then able to use their private key to reverse the encryption, getting back the same plain-text data that was the purpose of the message. 

But what if I want to be able to prove that it was me that sent that message in the first place? Public keys are, well, public. And how do I even know what the purpose of this encrypted data is without first decrypting it? That is a bit inefficient if I must decrypt the information before I even know what to do with it. Imagine dealing with that when writing up an API- chaos would quickly ensue. Introduce JWK’s. Here is an example of an ECDSA (Elliptic Curve Digital Signature Algorithm) JWK-

{
  "kty":"EC",
  "crv":"P-256",
  "x":"MKBCTNIcKUSDii11ySs3526iDZ8AiTo7Tu6KPAqv7D4",
  "y":"4Etl6SRW2YiLUrN5vfvVHuhp7x8PxltmWWlbbM4IFyM",
  "use":"enc",
  "kid":"1"
}

A JWK has several components:

A “kty” (Key Type Parameter) to specify what method was used to encrypt the data, most popular being RSA- “RSA” and ECDSA- “EC”.

The information that describes the actual public key. With ECDSA, that means saying what specific elliptical curve was used- “crv”, and then the X/Y- “x”/”y” coordinates of the public key on the graph. With an RSA JWK, instead of “crv” there is an “alg”, and then and “n” and “e” parameter, which serve the same purpose to tell you what the actual public key points are. With RSA it is not a graph you are describing however, but that is for another day.

A “use” parameter (*optional*) to specify what the key information that is supplied in the JWK is used for. Most of the type you will see either “sig”, which means the key is used to confirm the identity of whoever sent the message, or “enc”, which means is it to be used to encrypt data. 

The “kid” (*optional*) stands for Key ID. This is useful when storing multiple JWK’s to reference them. Look at that example JWK again. If you need to reference back to it at a later point, you’re going to want to know what this key is for.

There are several other parameters that can be used, and if you are interested you can check out the docs here: https://tools.ietf.org/html/rfc7517#appendix-A

Big picture, we use a JWK as only a single part of an encrypted message. Next week, we’ll zoom out even further and look at Json Web Tokens, which incorporate the JWK with the data that has actually been encrypted. 

So, in summary, a JWK is used to describe what the purpose of an encrypted message’s contents, how they have been encrypted, and then the public key that will be used for some purpose, described in the JWK. Imagine it as the instructions that come with your IKEA furniture- descriptive, instructive, and impossible to put the bookcase together without. 

