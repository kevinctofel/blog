---
layout: blog
title: "Interesting: Developing in Ubuntu through VS Code, running in WSL2"
date: 2020-07-18T20:29:58.859Z
thumbnail: /images/GitHub-repo-for-my-blog.png
---
Late last month, I said I'd be looking into WSL, or the Windows Subsystem for Linux, which is still a work in progress and available for Windows 10. 

If you're not familiar with WSL, it's an easy way to run just about any Linux distro in a VM within Windows. [Microsoft explains it better than I can](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).

The first version was a little slow due to the architecture, but now Microsoft has WSL2, which slips a very small but capable Linux kernel in the middle of the architecture, like so:

![Microsoft WSL2 architecture](/images/wsl-2-architecture.jpg)

This allows Windows 10 users to use Windows apps that interact quickly with Linux apps. For example, I installed and configured WSL2 and then grabbed Ubuntu from the Microsoft Store. (YES, the Microsoft Store is where you get the distros!)

I upgrade Ubuntu packages as needed and installed Node.js and Gatsby, which is what I'm using to experiment with an open source blog platform that generates super fast static sites: [More info here on what I'm doing](https://www.kctofel.com/post/2020-06-18-the-great-gatsby-vs-hugo-for-static-site-generation/).

I already had VSCode installed on the Windows side, by the way. And that's important. Here's why, in a general sense, per Microsoft:

> <!--StartFragment-->
>
> WSL 2 includes a huge architecture change using virtualization technology, and we are still working on improving the networking support. Since WSL 2 now runs in a virtual machine, you will need to use that VM’s IP address to access Linux networking applications from Windows, and vice versa you will need the Windows host’s IP address to access Windows networking applications from Linux
>
> <!--EndFragment-->