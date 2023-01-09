---
url: https://medium.com/mkdir-awesome/how-to-install-x86-64-homebrew-packages-on-apple-m1-macbook-54ba295230f
title: How to Install x86_64 Homebrew Packages on Apple M1 MacBook - by Shinichi Okada - mkdir Awesome - Medium
date: 2023-01-09 10:13:42
tag: 
summary: Using Rosetta, Homebrew, alias, and VSCode
---
## Using Rosetta, Homebrew, alias, and VSCode

![](https://miro.medium.com/max/1400/1*pTzpcuRbsKVZ7HegScFXiQ.png)

Photo by [Dynamic Wang](https://unsplash.com/@dynamicwang?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral). Image by the Author.

The New MacBook Air/Pro uses an Apple M1 chip. There are still many applications that support **only** Intel processors. You can check it by opening app information through the “Get Info” button.

![](https://miro.medium.com/max/624/1*87ClmTZ4S3UKDzAzDwK_Ig.png)

An app with “Application (Universal)” supports both Apple silicon and Intel processors. (It uses Apple silicon by default.) An app with “Application (Intel)” supports only Intel processors. An app with “Application (Apple Silicon)” supports only Apple silicon.

![](https://miro.medium.com/max/1400/1*JQULoAlar_JCBnI0xRCEmQ.png)

When you try to install a Homebrew package which depends on x86_64 architecture, you may have an error:

![](https://miro.medium.com/max/1400/1*mEXlyzhW7cfxe3OFCr0y2A.png)

Rosetta 2 enables a Mac with Apple silicon to use apps made for an Intel processor.

Install Apple Rosetta 2:

```
/usr/sbin/softwareupdate --install-rosetta
```

You can install Homebrew on M1 Mac as usual:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This will install Homebrew in the `/opt/homebrew/bin/brew` directory. When you install apps using Homebrew it installs them to the `/opt/homebrew/Cellar` directory and creates a symlink in the `/opt/homebrew/bin` directory.

When you install Homebrew on an Intel Mac, it installs in the `/usr/local/homebrew` directory.

Create a `~/Downloads/homebrew` and download Homebrew tarball and extract it to the `~/Downloads/homobrew` directory.

```
cd ~/Downloads
mkdir homebrew
curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
```

Move the `homebrew` directory to `/usr/local/homebrew`. You need the `sudo` command:

```
sudo mv homebrew /usr/local/homebrew
```

Add a path to the `.zshrc` file:

```
export PATH=$HOME/bin:/usr/local/bin:$PATH
```

By now you can use `arch -x86_64 /usr/local/homebrew/bin/brew` to install apps to the `/usr/local/homebrew/Cellar` directory.

Let’s add an alias and path in the `~/.zshrc` file:

```
# If you come from bash you might have to change your $PATH.
# need this for x86_64 brew
export PATH=$HOME/bin:/usr/local/bin:$PATH# for intel x86_64 brew
alias axbrew='arch -x86_64 /usr/local/homebrew/bin/brew'
```

Now you can install apps for Intel processors:

```
axbrew install package-name
```

You can use all brew commands:

```
axbrew list
axbrew reinstall package-name
axbrew --help
```

![](https://miro.medium.com/max/1400/1*WdjTWFUuKSOVAH2CQaBBXA.png)

![](https://miro.medium.com/max/1400/1*vWLVoksKb8OdB0rkjwf2pg.png)

Installing pyenv using an alias command for arch -x86_64 /usr/local/homebrew/bin/brew. Image by Author.

Some VSCode extensions require an executable path in the `settings.json` file. In my case, I needed to change `shellcheck.executablePath`.

```
"shellcheck.executablePath": "/usr/local/homebrew/Cellar/shellcheck/0.7.2/bin/shellcheck",
```

![](https://miro.medium.com/max/1400/1*peuv7nZu_CQqKd94G-ngbQ.png)

@[Eric Yang](https://medium.com/@ericleiyang?source=post_page-----a77f93c50381--------------------------------) showed a different way to install Homebrew in his “[5 Things I Have Learned Using the M1 MacBook Air](https://betterprogramming.pub/5-things-i-have-learned-when-using-the-m1-chip-macbook-air-a77f93c50381)” article. I hope this article shows you an easy alternative to manage two Homebrews on an M1 Mac.