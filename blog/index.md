# Haskell Blog

## Background
This blog is a progression of experiences related to learning about Haskell and programming languages. Before discussing anything about my experiences with Haskell and functional programming, it is important to establish some background. My computer is on Windows 10 Education, running with a 64-bit operating system, x64-based processor, and 12 GB RAM. I use Atom as my text editor.

Downloading Haskell on my computer proved to be simple. Following the steps on the [Haskell site](https://www.haskell.org/platform/) was adequate. To use Haskell, type `ghci` in your termianl. Haskell files end in .hs

Downloading BNFC on my computer required an addition step of changing my namespace to be on the Google namespace, because I wasn't able to ping anything. After hours of research, I have compiled what has worked for me. I had to do the following steps:
1. Open WSL as the administrator. 
2. Type `sudo bash` and enter your password.
3. Type `rm /etc/resolv.conf` to clear the current /etc/resolv.conf file.
4. Update the file to have the public namespaces by typing `echo nameserver 8.8.8.8 > /etc/resolv.conf` then `echo nameserver 8.8.4.4 >> /etc/resolv.conf`.
5. Verify that the changes have been made by typing `cat /etc/resolv.conf`.
6. To make the changes permanent (because I found that my /etc/resolv.conf file keep resetting itself to my IP), type `sudo apt-get install resolvconf` then `sudo gedit /etc/resolvconf/resolv.conf.d/base`. 

To run Linux, I used WSL as my terminal and followed the [official site](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install it.

## Table of Contents:

1. [Functional Programming](functionalprogramming.md)
2. [Pattern Matching](patternmatching.md)
3. [Parsing Trees](parsetrees.md)
4. [Lambda Calculus](lambdacalc.md)
5. [Abstract Reduction Systems](ars.md)
6. [Invariants](invariants.md)
7. [Measure Function](measurefunc.md)
8. Roman Numerals Rewriting
9. Fixed Point Combinator
10. Dafny
