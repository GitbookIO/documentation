# Custom Domains

**Gitbook.com** serves up your books under `http://{author}.gitbooks.io/{book}/`, and the book's content at `http://{author}.gitbooks.io/{book}/content/`.

You can also configure your book content to use a custom domain name, a free feature on GitBook. (It is currently not possible to use a custom domain name for homepage, or author page).

To add a custom domain you need administrative access to your domain name. If you don't have any clue how DNS works, get someone to help you with this.

These are the steps:

1. Set up a custom domain that points to "www.gitbooks.io".
2. Wait for this domain change to propagate (can take a few hours).
3. Configure your book to use this domain.

Note: if you do step (3) before step (1) then your book will be unreadable for several hours.

### Setting up a Custom Domain

You do this with your domain registrar's web interface.

1. Login to your domain registrar and find the page that allows you to add/edit host records. That page is often found in your settings under `Edit DNS`, `Host Records` or `Zone File Control`.

2. Set the `www` record to a **CNAME** and set the URL field to: ```www.gitbooks.io.``` with a trailing dot.

3. To **redirect** the naked domain (`yourdomain.com`) to `www.yourdomain.com`, you'll need to enable *"domain forwarding"*. This is often found under 'Forwarding', 'URL Forwarding' or 'URL Redirect'.

The raw zone file looks like this:

    www 10800 IN CNAME www.gitbooks.io.

### On GitBook.com

Go to your book's **Settings** tab and then click on **Domains**. Then enter your domain `www.yourdomain.com` and save.

![Add domain in settings](../assets/add_domain.png)

Test it right away by clicking on the link to your content. If this does not work. clear the domain name in your book's settings, save, and then ask for help. If you cannot click to see your content, no-one else can either.
