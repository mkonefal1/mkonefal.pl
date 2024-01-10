---
title: "Better way to blog, try Hugo"
date: 2024-01-10T01:58:33+01:00
---
## Wordpress is bloated
A few years ago, WordPress used to be the primary way of running a blog. Unfortunately, it's now considered a rather outdated tool that, in today's times, hinders more than it helps in creating online content. For novices, WordPress might be appealing due to its GUI editor and extensive admin panel. However, the majority of people who want to share their writings online won't utilize even 80% of WordPress's capabilities.

## The Key to Productivity is Simplicity
To publish content using WordPress or a similar tool, you have to put in quite a bit of effort. Using GUI tools may be easier for those unfamiliar with computers, but it significantly slows down work. Today, we don't have time for clicking through multiple windows; time is precious. That's where Static Site Generators come into play.

## What Exactly is a Static Site Generator?
SSG, or Static Site Generator, like Hugo, is a tool used for creating websites by generating static HTML files from templates and content, typically written in Markdown format. Unlike traditional Content Management Systems (CMS) that dynamically generate pages each time a user visits them, SSG pre-generates the pages in advance, resulting in fast-loading and less server load. Hugo is a popular SSG due to its speed, flexibility, and ease of use, making it an ideal tool for blogs, portfolios, and other sites where content doesn't change frequently.

## Why Hugo?
Because it's simple and popular. Of course, there is a wide range of SSGs like Zola, Jekyll, and others. However, since I use Hugo myself, I'll focus on it.

## How to Get Started?
First and foremost, you need to:
- Have a basic understanding of Git.
- Have an account on Github or an alternative service.
- Be familiar with the basics of writing documents in [Markdown](https://www.markdownguide.org/basic-syntax/).

### 1. Install the Necessary Programs
```
# Commands provided for Debian-based systems
sudo apt install git hugo
```

Additionally, you'll need a text editor in the command-line interface (I recommend Vim/Neovim, but Nano can also work).

### 2. Basics of Hugo

*I won't go into unnecessary details. Let's follow the Pareto principle (80% of the results can be achieved with 20% of the program's capabilities).*

The most important Hugo commands include:
- `hugo new site <site-name>` - creating the "skeleton" of your site.
- `hugo server` - running a local server to test your site.
- `hugo new <post-name>.md` - creating a new post on your site.
- `hugo` - simply running `hugo` generates your site, which you can then upload to a server using Git.

### 3. Choosing a Theme
Before launching your test site locally, you need to select a theme from [themes.gohugo.io](https://themes.gohugo.io/). Choose a theme that suits your preferences (I recommend something minimalist; I personally use [Holy](https://themes.gohugo.io/themes/holy/)).

### 4. Creating Your Site
Start by creating a repository on Github. Download it to your computer using the `git clone` command. In the repository folder, create the skeleton of your site with the `hugo new site <name>` command. Then, add your chosen theme to the repository using the `git add submodule` command. It's important to place the theme in the Themes folder.

Next, configure your site in the `config.toml` file. Most themes have sample configurations in their repositories. It's best to copy these and customize them to your needs.

Important: Fill in information about your theme first.
```
echo "theme = '<theme-name>'" >> config.toml
```

If everything has been done correctly, you can now run your local server using the `hugo server` command.

### 5. Adding Content
You can do this automatically or manually.

- Using the `hugo new posts/<post-name>.md` command generates a new Markdown file in the posts folder.
- Alternatively, you can create a new file manually in the folder.

The advantage of the first method is that it automatically generates a header with basic information such as title and publication date.

Sample header:
```
---
title = ""
date = ""
---
```

### 6. Generating the Site
Once you've written your first article, return to the main folder and generate the site with the `hugo` command. Now, all that's left is to push it to Github.

### 7. Where to Host Your Site
An ideal solution for SSGs is a service like [Netlify](https://www.netlify.com/), where you get around 100GB of space for free. You can attach a domain, which you can obtain inexpensively from a service like [OVH](https://www.ovh.com/). Then, connect your Github repository and follow the instructions on the website.

In just 30 minutes, you can enjoy a simple website. For more information, I recommend checking the [Hugo documentation](https://gohugo.io/documentation/), where more advanced techniques for creating a website are described.
