# How To <Task> with <Software> on <Distro>

### Introduction

This section should include two or three paragraphs. The first two paragraphs should include (but are not limited to) a brief introduction to the topic, a basic description of the technologies being used, and why the reader would want to read the article.

The last paragraph should summarize the goal of the article — In this guide, you will learn how to ...

## Goals (Optional)

You can include an optional **Goals** section if your tutorial has a complicated purpose, method, or result. Most articles do not need this section.

## Prerequisites

Introduce your prerequisites with a sentence or several paragraphs, as needed. Always use a bulleted list. Always include what type of Droplet is needed. This includes the operating system, the OS version, and any minimum resource requirements. Always use a non-root sudo user throughout your article unless the command must be executed by a specific user or by the root user.

Prerequisites should be things we need before we start. Look for existing DO articles on these prerequisites and link to them whenever possible.

Before you begin this guide you'll need the following:

- <OS and OS Version> Droplet
- A non-root user with sudo privileges (<insert link to Initial Server Setup article for the OS used in this tutorial>) explains how to set this up.)
- (Optional) If software such as Nginx needs to be installed, link to the proper article describing how to install it
- List any other accounts needed, such as Github or other services.

All the commands in this tutorial should be run as a non-root user. If root access is required for the command, it will be preceded by `sudo`. 

## Step 1 — Installing Some Cool Package

Always start each section with a transition/introductory sentence or paragraph. It is helpful to tell the reader what the goal of the current step is. Be careful not to repeat the wording of the step though.

If possible, the article should be organized into sequential steps. Try to use the "ing" form of the verb for the section titles. The section titles should have a consistent style to them: **Step 1 — Installing Some Cool Package**, **Step 2 — Configuring Some Cool Package**, **Step 3 — Securing Some Cool Package**, etc.

Try to break up the process into small steps. If there are multiple steps within the configuration section, consider making them individual steps.

### Header 3

H3 headers should be used sparingly. H4 headers should be avoided. If you need to use subheaders, make sure there are two or more headers of that level within that section of the tutorial.

## Commands

If the reader needs to execute a command, always show the command as a command block (where the command is on its own line) and use the following format:

```command
sudo nano /etc/nginx/sites-available/default
```

Be sure to explain what the command does after you give the command. DigitalOcean articles should be written with instructions alternating between explanations.

By default, all commands marked this way will be displayed with a gray background and a `$` prompt. If you need to use a custom prompt for the command block, use the following format:

```custom_prefix(>)
exit
```

## Inline Code

Filenames, package names, keypresses, and command line options should all be marked as `inline code`.

## Files and Scripts

To show the contents of a file or provide a script, using the following format:

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

Notice the filename in the label and notice the <^>custom tag<^> that will highlight the content in red. Always highlight the content that needs to be changed.

## Variables

You can highlight in-line variables <^>in red<^>. You can use in-line code formatting with variables if needed: `<^>variable<^>`

## Bold and Italics

Include bold or italics text as follows:

This text is **bold**.

This text is *italics*.

## Output

If you ask the reader to verify the output of a command, always include what the expected output should look like. It should be formatted as follows:

```
[secondary_label Output]
Could not connect to Redis at 127.0.0.1:6379: Connection refused
```

## Notes and Warnings

Notes and warnings are as follows:

<$>[note]
**Note:** This is a note.
<$>

<$>[warning]
**Warning:** This is a warning.
<$>

## Key Presses

Key presses should be written in ALLCAPS with in-line code formatting: `ENTER`.

Use a plus symbol (+) if keys need to be pressed simultaneously: `CTRL+C`.

## Links

Clickable links can be created with the following syntax: [Link Title] (http://www.example.com/)

## Screenshots

Screenshots should be in PNG format and have a maximum size of 745x745 pixels. Host them on imgur and embed them in the article using the following format:

![Alt text for screen readers](/path/to/img.png)

The images will be copied to a DO server when the article is published.

## Lists

Lists are simple:

- Item 1
- Item 2
- Item 3

## Transitions

At the end of each step, try to transition to the next step in the process whenever possible. It's helpful to remind the reader of what has been accomplished already and let them know what's ahead.  Steps that end with output or code snippets seem like they end abruptly. A single sentence that wraps up the step and moves to the next part helps the reader move forward. 
It's helpful to remind the reader of what has been accomplished already and let them know what's ahead.

## Conclusion

This article template should be used as a starting point when writing DigitalOcean tutorials. You should still refer to the style and formatting guidelines for more detailed explanations:

- [do.co/style](do.co/style)
- [do.co/formatting](do.co/formatting)

Readers should be able to follow your tutorial from the beginning to the end on a DigitalOcean Droplet. Before submitting your article to the editorial team, please be sure to create a new Droplet and test your article from start to finish on it exactly as written. Cut and paste commands from the article into your terminal to make sure there aren't typos in the commands. If you find yourself executing a command that isn't in the article, incorporate it into the article to make sure the reader gets the exact same results.
