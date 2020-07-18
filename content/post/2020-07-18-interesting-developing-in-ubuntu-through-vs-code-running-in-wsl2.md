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

I already had VS Code installed on the Windows side, by the way. And that's important. Here's why, in a general sense, per Microsoft:

> <!--StartFragment-->
>
> WSL 2 includes a huge architecture change using virtualization technology, and we are still working on improving the networking support. Since WSL 2 now runs in a virtual machine, you will need to use that VM’s IP address to access Linux networking applications from Windows, and vice versa you will need the Windows host’s IP address to access Windows networking applications from Linux.
>
> <!--EndFragment-->
>
> What this effectively means is: I can use Nodejs, Gatsy, or anything else I want in Linux but actually do so through VSCode in Windows. That's because VSCode is running as a remote server to the Linux instance! 
>
> ![VSCode in Windows accessing Node.js and Gatsby in Ubuntu](/images/gatsby-in-wsl2.jpg "VSCode in Windows accessing Node.js and Gatsby in Ubuntu")
>
> In the example above, I did a simple "Hello world" blog post / page as you can see in VSCode. But look at the bottom left of the app: You can see that VSCode is actually working with the Ubuntu filesystem, which is where I have Node.js and Gatsby installed. 
>
> Whoa!
>
> I'm just kicking the tires right now but this is an interesting approach from Microsoft. 
>
> I use a similar solution on my Chromebooks, which Google debuted about two years ago with something called "Project Crostini". Essentially, it's a Linux container running in a VM that looks completely native to Chrome OS. There's an added benefit to Crostini at the moment: I can run Linux GUI apps with it alongside of the Chrome OS applications. So on a Chromebook, I would simply run VSCode in Linux to replicate the above.
>
> I've written extensively about Crostini on Chromebooks but the most recent and useful piece is this one, if you're interested: ["Can you learn to code in a college Computer Science program with a Chromebook?](https://www.aboutchromebooks.com/news/can-you-learn-to-code-in-a-college-computer-science-program-with-a-chromebook/)"
>
> ![Linked Lists in Java on a Chromebook](/images/linked-lists-in-java-on-a-chromebook.jpg "Linked Lists in Java on a Chromebook")
>
> I have to give a shoutout to Scott Hanselman because he's been sharing information, tips and tricks about WSL for more than a year. And although this video of his is rather long at 45-ish minutes, I learned more than 45 things about WSL.
>
> <iframe width="560" height="315" src="https://www.youtube.com/embed/j0PPcUUtHlw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
>
>