# Agency Theme 

#### NOTE: This theme has been archived

The development of this theme has been discontinued on 07.08.2019. The repository is archived in its current state. In this state it will not be possible to create new pull requests or issues. However, feel free to fork this theme.

[Syna](https://syna.okkur.org) has been developed by [Michael Grosser](https://github.com/stp-ip) as a flexible evolution of the Agency theme. Please consider to use it for new projects instead.

Thanks to all contributors who have helped to improve this theme.

---

Agency Theme is a one page projets for companies and freelancers based on the [original Bootstrap theme](//github.com/IronSummitMedia/startbootstrap-agency) by [David Miller](//github.com/davidtmiller). This Hugo theme features several content sections, a responsive projets grid with hover effects, full page projets item modals, a timeline, and a contact form.



![Hugo Agency Theme screenshot](https://raw.githubusercontent.com/digitalcraftsman/hugo-agency-theme/master/images/screenshot.png)


## Installation

Inside the folder of your Hugo site run:

    $ cd themes
    $ git clone https://github.com/digitalcraftsman/hugo-agency-theme

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.


## Getting started

After installing the Agency Theme successfully it requires a just a few more steps to get your site running.


### The config file

Take a look inside the [`exampleSite`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/exampleSite) folder of this theme. You'll find a file called [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml). To use it, copy the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml) in the root folder of your Hugo site. Feel free to change the strings in this theme.


### Change the hero background

The hero acts as an eye-catcher for your site. So consider to give him a nice background. You just need to replace the [`header-bg.jpg`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/static/img/header-bg.jpg) at [`static/img`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/static/img) with your own background image. But it's important that you keep the original filename.


### Present your skills

This section should show your capabilities and skills. You can change the services at `[params.services.list]` in the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml).

All icons are part of Fontawesome's icon font. Look at the website of [Fontawesome](//fortawesome.github.io/Font-Awesome/icons/) for more icons. The icons are represented by their corresponding CSS class of Fontawesome. A skill is defined like this example:

```toml
[[params.services.list]]
      icon = "fa-shopping-cart"
      title = "E-Commerce"
      description = "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima maxime quam architecto quo inventore harum ex magni, dicta impedit."
```


### Create your projets

Beside the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml), there is under `data` another subfolder called [`projects`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/exampleSite/data/projects) which hosts the files that will appear as your projects in the projets section. Such a project file might look like [this one](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/data/projects/2014-07-05-project-1.yaml) written in YAML:

```yaml
modalID: 1
title: Round Icons
subtitle: Lorem ipsum dolor sit amet consectetur.
date: 2014-07-05
img: roundicons.png
preview: roundicons-preview.png
client: Start Bootstrap
clientLink: "#"
category: Graphic Design
description: Use this area to describe your project. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est blanditiis dolorem culpa incidunt minus dignissimos deserunt repellat aperiam quasi sunt officia expedita beatae cupiditate, maiores repudiandae, nostrum, reiciendis facere nemo! <br><br>**Want these icons in this projets item sample?** You can download 60 of them for free, courtesy of [RoundIcons.com](//getdpd.com/cart/hoplink/18076?referrer=bvbo4kax5k8ogc), or you can purchase the 1500 icon set [here](//getdpd.com/cart/hoplink/18076?referrer=bvbo4kax5k8ogc).
```

Copy [`projects`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/exampleSite/data/projects) inside the `data` folder in the **root** directory of your site. Let's make some changes.

Pay attention to the `modalID`. It must be a unique integer and be incremented with each new project you want to add to the projets. Otherwise, the corresponding modal can't be rendered.

Furthermore, you can use Markdown syntax for URLs like here `[text](//url.to/source)` in the description.

To give your projects an image, save those under [`static/img/projets`](github.com/digitalcraftsman/hugo-agency-theme/tree/master/static/img/projets). Don't forget to set the appropriate **filename** under `img` in your project.


### Show what happened

This theme features a timeline for important events in your company or your career too. You can add a new event by copying the following snippet to the `[params.about]` section in the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml).

```toml
[[params.about.events]]
      img = "1.jpg"
      date = "2009-2011"
      title = "Our Humble Beginnings"
      description = "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt ut voluptatum eius sapiente, totam reiciendis temporibus qui quibusdam, recusandae sit vero unde, sed, incidunt et ea quo dolore laudantium consectetur!"
```

The image set under `img` needs to be stored at [`static/img/about`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/static/img/about). The events will be listed from the top to the bottom.


### Introduce your team

Let the visitors or potential clients know who you are. To add a team member paste the code below into the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml). The `img` field refers to the shown image. Paste those of you or your colleages into [`static/img/team`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/static/img/team) 

```toml
[[params.team.members]]
    img = "1.jpg"
    name = "Kay Garland"
    position = "Lead Designer"
    social = [
        ["fa-twitter", "#"],
        ["fa-facebook", "#"],
        ["fa-linkedin", "#"]
    ]
```

As you can see there's an option to link individual social networks. The first index of the array represents the icon (or CSS class) of [Fontawesome](//fortawesome.github.io/Font-Awesome/icons/). The last index is simply the link to the social network profiles.


### List your clients

You can also show some of your clients. To do so, paste the client's logos into [`static/img/logos`](//github.com/digitalcraftsman/hugo-agency-theme/tree/master/static/img/logos) and add the example below to the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml).

```toml
[[params.clients]]
    logo = "designmodo.jpg"
    link = "#"
```

***The logos require a dimension of 200 x 50 pixels.***


### Make the contact form working

Since this page will be static, you can use [formspree.io](//formspree.io/) as proxy to send the actual email. Each month, visitors can send you up to one thousand emails without incurring extra charges. Begin the setup by following the steps below:

1. Enter your email address under 'email' in the [`config.toml`](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/exampleSite/config.toml)
2. Upload the generated site to your server
3. Send a dummy email yourself to confirm your account
4. Click the confirm link in the email from [formspree.io](//formspree.io/)
5. You're done. Happy mailing!


### Nearly finished

In order to see your site in action, run Hugo's built-in local server. 

    $ hugo server

Now enter [`localhost:1313`](http://localhost:1313/) in the address bar of your browser.


## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](//github.com/digitalcraftsman/hugo-agency-theme/issues) to let me know. Or make directly a [pull request](//github.com/digitalcraftsman/hugo-agency-theme/pulls).


## License

This theme is released under the Apache License 2.0 For more information read the [License](//github.com/digitalcraftsman/hugo-agency-theme/blob/master/LICENSE).


## Acknowledgements

Thanks to 

- [David Miller](//github.com/davidtmiller) for creating this theme
- [Steve Francia](//github.com/spf13) for creating Hugo and the awesome community around the project
- [Michael Grosser](https://github.com/stp-ip) for contributing a significant amount of improvements
