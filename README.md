# OopsKit

### Maintenance pages for your website

A simple, responsive maintenance page that informs visitors when your website is undergoing maintenance or updates. The page features a modern design with both light and dark mode support.

## Preview

When active, visitors will see a friendly message indicating that the site is under maintenance

![Page preview](./assets/preview.png)


## Usage with Cloudflare

If you're using Cloudflare for your site, you can use the GH Pages url as the redirected landing page when your site is under maintenance.

This is a great way to keep your entire site:pages, assets, API etc. offline while you work on the maintenance.

1. Go to your Cloudflare dashboard and create a new page rule under Rules > Page Rules.
2. Set the page rule url to *.yoursite.com/* and the destination URL to the GH Pages url (https://thinkdj.github.io/oops-kit/) so that all requests to your site are redirected to the maintenance page. 
![Cloudflare Page Rule](./assets/cloudflare_pagerule.png)
3. Set the redirect type to "302 - Temporary Redirect".
4. Save the page rule and disable it when your site is no longer under maintenance.

## Alternate usage

If you're not using Cloudflare, you can still use this page as a temporary landing page when your site is under maintenance by self hosting it on your own server.

1. Temporarily replace your main index file with these files during maintenance periods (`index.html` and `styles.css`)
2. Customize the message in `index.html` and/or modify colors and styles in `styles.css` to match your brand if needed

## File Structure

```
├── index.html          # Main HTML file
├── styles.css          # CSS styles with dark mode support
└── README.md           # Documentation
```

## Customization

### Changing the Message

Edit the text in `index.html`:

```html
<h1>We'll Be Right Back</h1>
<p>Our site is currently undergoing maintenance...</p>
```

### Modifying Colors

The color scheme can be customized in `styles.css`. The file includes both light and dark mode color variables.

## Browser Support

- ✅ Modern browsers (Chrome, Firefox, Safari, Edge)
- ✅ Mobile browsers
- ✅ Dark mode support through `prefers-color-scheme`

## License

Feel free to use this maintenance page for your projects. Attribution is appreciated but not required.

You can even temporarily use the GH Pages url as your redirected landing page when your site is under maintenance.


> 🕊️
