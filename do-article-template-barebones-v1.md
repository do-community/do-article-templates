# Use Title Case for all Titles

### Introduction

Introductory paragraph.

In this guide, you will learn how to ...

When you're finished, you'll be able to...

## Prerequisites

Introductory paragraph

Before you begin this guide you'll need the following:

- <OS and OS Version> Droplet
- A non-root user with sudo privileges (<insert link to Initial Server Setup article for the OS used in this tutorial>) explains how to set this up.)
- (Optional) If software such as Nginx needs to be installed, link to the proper article describing how to install it
- List any other accounts needed, such as Github or other services.

All the commands in this tutorial should be run as a non-root user. If root access is required for the command, it will be preceded by `sudo`. 

## Step 1 — Title Case

Introduction to the step. What are we going to do?

Content. Here are examples.

Here's a command someone types in the Terminal:

```command
sudo nano /etc/nginx/sites-available/default
```

Here's a custom prefix:

```custom_prefix(>)
exit
```

Here's a configuration file with a label:

```
[label /etc/nginx/sites-available/default]
server {
    listen 80 default_server;
    listen [::]:80 default_server ipv6only=on;

    root <^>/usr/share/nginx/html<^>;
    index index.html index.htm;

    server_name localhost;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

Here's output from a command:

```
[secondary_label Output]
Could not connect to Redis at 127.0.0.1:6379: Connection refused
```

This is a <^>variable<^>. 

This is `inline code`.

This is an `<^>in-line code variable<^>`

Use `<^>your_server_ip<^>` when referencing the IP of the server.  Use `111.111.111.111` and `222.222.222.222` if you need other IP addresses in examples.

This text is **bold**.

This text is *italics*.

Key presses should be written in ALLCAPS with in-line code formatting: `ENTER`.

Use a plus symbol (+) if keys need to be pressed simultaneously: `CTRL+C`.

<$>[note]
**Note:** This is a note.
<$>

<$>[warning]
**Warning:** This is a warning.
<$>

Clickable links can be created with the following syntax: [Link Title] (http://www.example.com/)

Screenshots should be in PNG format and have a maximum size of 745x745 pixels. Host them on imgur and embed them in the article using the following format:

![Alt text for screen readers](/path/to/img.png)

Lists are simple:

- Item 1
- Item 2
- Item 3


Now transition to the next section.

## Step 2 — Title Case

Another introduction

Your content

Transition. 

## Conclusion

This is a barebones article template that can be used as a quick starting point when writing DigitalOcean tutorials. If you are not already familiar with Markdown, you should use our more detailed article template or refer to the style and formatting guidelines for more detailed explanations:

- [do.co/style](do.co/style)
- [do.co/formatting](do.co/formatting)

Readers should be able to follow your tutorial from the beginning to the end on a DigitalOcean Droplet. Before submitting your article to the editorial team, please be sure to create a new Droplet and test your article from start to finish on it exactly as written. Cut and paste commands from the article into your terminal to make sure there aren't typos in the commands. If you find yourself executing a command that isn't in the article, incorporate it into the article to make sure the reader gets the exact same results.
