---
layout: post
title:  "Ditch your stone age password! Security keys and new technology"
date:   2023-08-24 00:00:01 +0100
tags: IT security 2fa fido yubikey
---
![Security Keys scattered over a desk](/assets/blog/Unsplash-Yubikey.jpg)

I have long been an admirer of the benefits hardware-backed security keys give you. Being able to physically hold they key to some of your most important online accounts is not only an amazing thing to think about, but an amazing thing for security too. I'm not saying that standard TOTP codes are bad, but there's still a one-in-a-million chance that a computer could guess the code right - and if the service hasn't implemented a restriction on the number of times a code can be guessed, its just a waiting game.

## What is a security key?
It's essentially what it says on the tin. A small device, usually with a USB connector of some sort on it, which can be used to secure your accounts using a physical thing - a literal key to your online accounts. It means that people won't be able to gain access to your account if they aren't physically holding that key. They have other benefits, too.

Due to the way they authenticate with each different website, they stop phishing attacks. You can't be phished if you have one of these linked to your account - it's a bold statement, but I'm willing to stand by it. These keys generate a unique 'hash' for each service, and one of the things this hash is based on is the domain of the website you are logging in to - so the one for 'facebook.com' is very different to the one for 'facebok.com'. Obviously though, still don't go entering all of your Google account credentials into a Google Form.

## How do they work?
There are many different standards these small devices support, but the most popular is U2F (Universal Second Factor).

![U2F Diagram](/assets/blog/FIDO-Diagram.png)

Above shows a simplified diagram of how this standard works. One you have entered your username/password, the service sends a 'challenge' to the security key. Once it has received the challenge, it processes it and digitally signs it in a way which proves that it was done by the authorised security key. After that, it sends back the challenge and you gain access to the service!

## The YubiKey
I was lucky enough to be able to purchase 2 YubiKeys lately and have just finished setting them up on all of my online accounts which support them. Once the initial setup was complete (which was a little inconvenient thanks to Windows, well, being Windows) I found it very easy to integrate into my workflow and felt the benefits almost instantly. Logging into GitHub? No more navigating through your phone to find and then type your TOTP code - simply plug in my YubiKey and press the little circle. Not only is it more secure but it's so much more convenient!

It's just as easy to sign into services on your phone, too. I have NFC enabled YubiKeys and with iOS and Android supporting them natively, it's as simple as a tap on the back of your phone and - boom. You're in!

## New Technology: Passkeys
Just over a year ago, Apple announced they've been working alongside other tech companies to make a new standard for authentication, known as passkeys. They essentially act like a wireless security key which is built into your phone. A service will present to you a QR code which you just scan on a device which you have registered to hold your passkey and you have been authenticated. This is a huge step forward for the security space of online services as not only will it make it more accessible, as everyone who owns an iPhone 8 or later now has free access to them in iOS 16 (with Android support being rolled out now aswell), but it will make it more normal. If your mobile OS is recommending you use passkeys instead of TOTP (or nothing) then it will take away the notion that you have to be some high-profile activist who is actively being targeted by the Russian government for these to be effective for you.

However over a year later, I don't see many services offering this perfect passwordless authentication approach just yet. Apple have started offering passwordless login on their own sites recently so I am hoping to see others follow suit in the near future, too.

## The problem (and ideal solution)
Now I have sugar coated the hell out of this technology, lets talk about the elephant in the room, the support for these devices. While you can secure all of your main accounts, such as Google, Microsoft, Facebook, Twitter and even some online services such as GitHub, Cloudflare and Namecheap, the list doesn't go on for much longer. Personally, I believe this is just because of the lack of large-scale adoption. While you may see these out and about from time-to-time, there just isn't enough volume for most small or medium sized companies to put in the effort of supporting and maintaining such a service, unless they handle a very security-centred part of a very small market.

Overall, I would still recommend the use of security keys and/or passkeys to everyone I know. They just give you that extra piece of mind that you are not going to be responsible for your grandma's phone number being sold on the dark web, or worse off, your bank account being drained. Hopefully, through iOS 16 and newer versions of Android releasing these technologies to the masses, more and more sites and apps (cough, cough, banking services) will begin to support this technology and leverage the benefits it has over traditional authentication.