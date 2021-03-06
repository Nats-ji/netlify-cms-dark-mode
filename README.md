<a href="https://www.buymeacoffee.com/mingm"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=mingm&button_colour=FF5F5F&font_colour=ffffff&font_family=Comic&outline_colour=000000&coffee_colour=FFDD00" width="180px"></a>

# Netlify CMS Dark Mode Theme

## What is this?

This is a simple CSS file that you can add to your Netlify CMS's HTML file.

It automatically toggles your Netlify cms to dark mode if your system is also set to dark mode.

You can view the demo site [here](https://nats-ji.github.io/netlify-cms-dark-mode/).

![image](https://user-images.githubusercontent.com/13299626/110656997-708d1280-81fb-11eb-8c50-a9bd35596a82.png)

## Who is this for?

This is mainly for people who install the Netlify CMS with javascript from the CDN. Since there are more limitations with customization.

But you can also use this with the npm installation method. However, it's better to write a separate package.

## How to use?

### Method 1. Use CDN

Pull `dark.css` from a public cdn, so it will keep up-to-date. `https://cdn.jsdelivr.net/gh/Nats-ji/netlify-cms-dark@master/dark.min.css`

- Edit your Netlify CMS's HTML code:

   ```html
     </body>
     <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Nats-ji/netlify-cms-dark-mode@master/dark.min.css">
   </html>
   ```

### Method 2. Download

This method gives you more flexablity for making customizations.

1. Download [dark.css](https://github.com/Nats-ji/netlify-cms-dark-mode/blob/master/dark.css), and copy it to your site.

2. Open your Netlify CMS's HTML file.

3. Link `dark.css` behind the `</body>` tag.
   ```html
     </body>
     <link rel="stylesheet" href="./dark.css">
   </html>
   ```
   
You can check the demo HTML source code [here](https://github.com/Nats-ji/netlify-cms-dark-mode/blob/gh-pages/index.html).
   
## Change theme color?

- Just edit the css vars in `dark.css`!
   ```css
   :root {
     --body-bg-color: black;
   }
   ```
   
- If you want always dark mode instead of following the system's setting. You can remove the following code from `dark.css`:
   ```css
   @media (prefers-color-scheme: dark) {

   }
   ```

## Something is wrong?

You are welcome to make a Pull Request to fix any bugs or make any improvements.
