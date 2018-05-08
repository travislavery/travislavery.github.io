---
layout: post
title:      "ECDSA Encryption"
date:       2018-05-08 17:50:50 +0000
permalink:  ecdsa_encryption
---


ECDSA - Elliptic Curve Digital Signature Algorithm. 

Over the past several weeks, I've had the opportunity to delve into the various ways to encrypt, sign, and transfer information securely over the web. Right now, most people use something called RSA (Rivest–Shamir–Adleman) as their public-private key cryptosystem. Because of increasing computing power of computers in the modern age, it is becoming a question as to how viable this type of encryption will continue to be as computers get more and more capable of decryption attacks of RSA keys.

ECDSA is a different algorithm and method to accomplish the same mission of transmitting information securely. The math behind that powers this type of encryption is awesome. To oversimplify, pretty much what is happening is that because of the shape of elliptic curves, you can pick any 2 points on the curve (first point will be the private key, second point will be the public key), draw a line that intersects both points, and that same line will cross only 1 other point on the curve. The curve is symmetrical across the X axis, if that 3rd point was, for example, at (4, 7), there would be a point at (4, -7) that also fell on the curve. Use this new point, draw a line that intersects it and your 1st point, you’ll get a 3rd point, cross back across the X axis to it’s matching point, repeat. The reason that this is an effective way to encrypt data is that it is just about impossible to figure out where you started, and how many times you went back and forth across the X axis. If you do know where you started, however, it’s rather simple.

![](https://devcentral.f5.com/Portals/0/Users/184/04/114104/elliptic_curve_thumb.png)
*Image from devcentral.f5.com*

That is of course a bit simplified, but it’s dang cool. What has consumed a majority of my time as I’ve been working with using ECDSA is that when you are transferring information across the internet, you can’t just bombard whoever it is that you are sending information with a bunch of encrypted data and no context on what it is, what type of encryption it is, which algorithm or curve you used, and what information is required to decrypt it. There is also a signature that proves that it was, in fact, you that sent all this stuff to begin with. 

What I’m describing above is a JSON Web Key (JWK), and the topic for my next blog post. It’ll be a blast, I promise. 

If you want a more detailed and accurate explination of ECDSA, check out these youtube videos- 
* https://www.youtube.com/watch?v=NF1pwjL9-DE
* https://www.youtube.com/watch?v=dCvB-mhkT0w
