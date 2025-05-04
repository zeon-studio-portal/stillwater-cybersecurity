# Stillwater Cybersecurity

## Prerequisites
You need to fulfill some prerequisites to configure your machine, before you start with this project.


1. [Install Hugo](https://gohugo.io/getting-started/installing/)
2. [Install Go](https://golang.org/dl/)
3. [Install Nodejs](https://nodejs.org/en/download/)

## Clone The Repository and Install Dependencies
To clone the repository, run the following command:

```bash
git clone repository-url
cd my-project
```

To install dependencies, run the following command:

```bash
npm install
```

## Run The Project Locally
To run the project locally, run the following command:

```bash
npm run dev
```



## Colors, Fonts and Plugins
To change website colors, fonts, and plugins. Please open the my-project/hugo.toml file.

Change Website Colors
----------------------------
Under the params.variables section, you will have all the parameters to change the website color preferences. For example, if you change the value of color_primary, the primary color of the whole website.

example code:

```toml
[params.variables]
color_primary = "green"
color_secondary = "#001111"
body_color = "#fff"
text_color = "#666666"
text_dark = "#222222"
text_light = "#959595"
border_color = "#ACB9C4"
black = "#000"
white = "#fff"
light = "#fdfdfd"
```

Change Website fonts
-------------------
Below the color variables, you will get the font variables, and you can change the value of those variables as per your requirements.

Visit Google Fonts to see the fonts that are available to you. Then select the font you want to use. Then copy the bold part of the URL and paste it in the font_primary field. It will change the font of the website’s primary text. [google-fonts](https://fonts.google.com/)

If you want to change the value of the primary font type, you can change it to either sans-serif or serif as per your requirement.

example code:
```toml
font_primary = "Roboto:ital,wght@0,300;0,400;1,400"
font_primary_type = "sans-serif" # [serif/sans-serif]
font_secondary = "Work+Sans"
font_secondary_type = "serif" # [serif/sans-serif]
icon_font = "Font Awesome 5 Free" # chose icon: https://fontawesome.com/icons
```
font_size and font_scale is pretty new to our themes. It’s changed the full website font size. learn more about it here. We have added the whole system of font sizes to our theme. So you can change the font sizes as per your requirement direct from config.toml.

example code:
```toml
# base font size for full website 
font_size = "16px" # default is 16px
font_scale = "1.25" # default is "majorThird": 1.25
# Font Scale Sizes
# "minorSecond": 1.067,
# "majorSecond": 1.125,
# "minorThird": 1.2,
# "majorThird": 1.25,
# "perfectFourth": 1.333,
# "augmentedFourth": 1.414,
# "perfectFifth": 1.5,
# "goldenRatio": 1.618
```
Third-Party Plugins
-------------------
You can add or remove third-party plugins from here. We create a loop for plugins. You can see two plugins loops here, the first one is for css, and the last one is for js.

Sometimes you need to close the Hugo server and run again for rendered correctly.

### CSS plugins
```toml
[[params.plugins.css]]
link = "https://cdn.examplesite.com/your-plugin.css"
attributes = "your-attributes" # optional field

js plugins
[[params.plugins.js]]
link = "https://cdn.examplesite.com/your-plugin.js"
attributes = "your-attributes" # optional field
```


## Basic Configuration

Here is the default configuration and basic parameters for your website. You can change those as per your requirements.

### Default Configuration

In this project folder, you will find a file called `hugo.toml`. Open this file in any text editor or IDE.

- **baseURL**: Add your site URL here. Remember to add a trailing slash at the end of the URL.
- **languageCode**: Defines your global site language. For more information, see [Official Hugo Docs](https://gohugo.io/documentation/).
- **title**: The main title of your website.
- **theme**: Sets up the used theme. If your theme is located in `my-project/themes/theme-name` folder, then the value for this parameter is `theme-name`.
- **summaryLength**: Decides how many words are in excerpts of your posts when displayed as a preview. The default is 70 words.
- **paginate**: Set the number of posts shown on blog overview pages. Pagination will be visible for more posts.
- **disqusShortname**: Add your Disqus shortname to enable comments on the blog section. Follow this [tutorial](https://help.disqus.com/en/articles/1717111) to install Disqus.
- **googleAnalytics**: Add your Google Analytics ID to enable analytics on all pages. Example: `UA-123-45`. If you want another third-party analytics, you can contact us for custom service.
- **timeZone**: The default time zone for timestamps. Use any valid [TZ database name](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).


### Default Parameters

In this project folder, you will find a file called `config/_default/params.toml`. Open this file in any text editor or IDE.

- **favicon**: Path to your website's favicon. Place it in the `assets/images` folder.
- **logo**: Path to your website's logo. Place it in the `assets/images` folder.
- **logo_width**: Defines the width of the logo in pixels. Doesn’t work with `.svg` files.
- **logo_text**: Appears only if the logo parameter is missing.
- **description**: Default meta description, shown on pages without a meta description.
- **author**: The website author name, used in the meta author tag.
- **image**: Fallback for open graph and Twitter card if a page has no image of its own.
- **contact_info**: Fields like phone, email, and address for footer and contact page.
- **mainSections**: Section names to show on your website. It's an array; add more sections as needed. See [Official docs](https://gohugo.io/documentation/) for more info.
- **contact_form_action**: Activate your contact form with a third-party service like Airform, Formspree, or Formsubmit. Example Airform action: `https://airform.io/your@email.com`.
- **copyright**: Text at the bottom of the page.
- **preloader**: Enable or disable the preloader. If you want an image, logo, or animation, provide the file location, e.g., `preloader = images/preloader.gif`.
- **navigation_button**: Enable or disable the main navigation button.
- **social**: Loop item for social icons using Font Awesome. Choose more icons from [here](https://fontawesome.com/icons).
- **cookies**: Set cookie consent message and expiry days here.


## Content Management
You will get every page that your website has in the content folder. The content folder is a subfolder of the project folder.

### Homepage
Content folder contains the root file as _index.md. Open this page in any text editor, and you will be able to edit it. Some of the sections can hide. You can change its enable value to false.

### Other Pages
There are two types of pages in the Hugo theme, list page, and single page. The list page is kind of a landing page (ex: about page). And the single page is called the inner page of a product or a post (ex: blog single page). We need to define the structure or markup of every page.

We already provided the necessary markup for the existing pages. You can find the markup in the themes/layout folder. For example, Career page layout is layout: career. We have also provided default list and single page layouts. So when you create a new page, you don’t need to define the layout. It will be the default layout.


## 🚀 Build And Deploy
After you finish your development, you can build or deploy your project almost everywhere. Let's see the process:

### 👉 Build Command
To build your project locally, you can use the following command.

```bash
npm run build
```
### 👉 Deploy Site
We have provided 5 different deploy platform configurations with this template, so you can deploy easily.

- [Netlify](https://www.netlify.com/)
- [Vercel](https://vercel.com/)
- [Github Actions](https://github.com/features/actions)
- [Gitlab Ci](https://docs.gitlab.com/ee/ci/)
- [AWS Amplify](https://aws.amazon.com/amplify/)

And if you want to Host some other hosting platforms. then you can build your project, and you will get a public folder. that you can copy and paste on your hosting platform.

`Note: You must change the baseURL in the hugo.toml file. Otherwise, your site will not work properly.`



