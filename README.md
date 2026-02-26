# GitHub SSH Setup Guide

This repository documents how to push code from a local machine to GitHub using *SSH authentication*, along with the benefits of using SSH over HTTPS.

---

## Why Use SSH with GitHub?

Using SSH to interact with [GitHub](chatgpt://generic-entity?number=0) provides several advantages:

- No need to enter username or password for every push
- More secure authentication using public/private key cryptography
- Ideal for automation, scripting, and CI/CD pipelines
- Commonly used in Linux system administration and DevOps environments
- One-time setup works for all repositories

---

## Prerequisites

- Git installed
- A GitHub account
- Access to a Linux terminal, macOS terminal, or Git Bash on Windows

---

## Steps to follow:

- Open terminal, type ssh-keygen: if the key isn't created beforehand
- Start ssh agent, type ssh-add ~/.ssh/id_ed
- ls ~/.ssh, to view the key folder
- You will see id_ed.pub or rsa.pub thats the public key, type cat ~/.ssh/id_ed.pub
- Copy the output
- Go to github, open settings, SSH and GPG keys, new ssh key, paste the key, give it a name, save

---
- ssh -T git@github.com, to verify your connection 
- git remote add origin git@github.com:USERNAME/REPO.git, to add url and username 
- git remote -v, to verify url
- git branch -M main, to change brach name from master to main->makes it easier to push and pull 
- git push -u origin main, to push your repo
- Open github and you will see your repo
