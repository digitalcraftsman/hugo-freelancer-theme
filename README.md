# Freelancer Theme

Freelancer Theme is a one page freelancer portfolio based on the [original Bootstrap theme](//github.com/IronSummitMedia/startbootstrap-freelancer) by [David Miller](//github.com/davidtmiller) and on [Jerome Lachaud](//github.com/jeromelachaud)'s [Jekyll theme](//github.com/jeromelachaud/freelancer-theme). This Hugo theme features several content sections, a responsive portfolio grid with hover effects, full page portfolio item modals and a contact form.


## Contents

- [Installation](#installation)
- [Getting started](#getting-started)
  - [The config file](#the-config-file)
  - [Create your portfolio](#create-your-portfolio)
  - [Make the contact form working](#make-the-contact-form-working)
  - [Nearly finished](#nearly-finished)
- [Contributing](#contributing)
- [License](#license)


## Installation

Inside the folder of your Hugo site run:

    $ mkdir themes
    $ cd themes
    $ git clone https://github.com/digitalcraftsman/hugo-freelancer-theme

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.


## Getting started

After installing the Freelancer Theme successfullyi it requires a just a few more steps to get your site running.


### The config file

Take a look inside the [`example`](//github.com/digitalcraftsman/hugo-freelancer-theme/tree/dev/examples) folder of this theme. You'll find a file called [`config.toml`](//github.com/digitalcraftsman/hugo-freelancer-theme/blob/dev/examples/config.toml).
It contains detailed information about the setup of the contact form ([see below](#make-the-contact-form-working)) and the customization of all strings of this template. 

To use it, copy it in the root folder of your Hugo site.


### Create your portfolio

Beside the config file there is another subfolder called [`projects`](//github.com/digitalcraftsman/hugo-freelancer-theme/tree/dev/examples/projects) which hosts the files that will appear
as your projects in the portfolio section. Such a project file might look like [this](//github.com/digitalcraftsman/hugo-freelancer-theme/blob/dev/examples/projects/2014-07-18-project-1.yaml):

```yaml
modalID: 1
title: Project Cabin
date: 2014-07-18
img: cabin.png
client: Start Bootstrap
category: Web Development
description: Use this area of the page to describe your project. The icon above is part of a free icon set by [Flat Icons](//sellfy.com/p/8Q9P/jV3VZ/"). On their website, you can download their free set with 16 icons, or you can purchase the entire set with 146 icons for only $12!
```

Copy the folder [`projects`](//github.com/digitalcraftsman/hugo-freelancer-theme/tree/dev/examples/projects) inside the `data` folder in the root directory of your site. Let's make some changes to show your work.

Pay attention to the `modalID`. It must be a unique integer and be incremented with each new project you want to add to the portfolio. Otherwise the corresponding modal can't be rendered.

Furthermore you can use Markdown syntax for URLs like here `[text](//url.to/source)` in the description. Copy the image of an project inside `static/img/portfolio` and **just** enter the filename.


### Make the contact form working

Since this page will be static, you can use [formspree.io](//formspree.io/) as proxy to send the actual email. Your visitors can send up to a thousand emails each month for free to you. Follow the steps below:

1. Enter your email address under 'email' in the config.toml
2. Upload the generated site to your server
3. Send a dummy email youself to confirm your account
4. Click the confirm link in the email from www.formspree.io
5. You're done. Happy mailing!


### Nearly finished

In order to see your site in action, run Hugo's builtin local server. 

    $ hugo server -w

Now enter `localhost:1313` in the address bar of your browser.


## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](//github.com/digitalcraftsman/hugo-freelancer-theme/issues) to let me know. Or make directly a [pull request](//github.com/digitalcraftsman/hugo-freelancer-theme/pulls).


## License

This theme is released under the Apache License 2.0 For more information read the [License](//github.com/digitalcraftsman/hugo-freelancer-theme/blob/master/LICENSE).

Thanks to [Steve Francia](//github.com/spf13) for creating Hugo.
