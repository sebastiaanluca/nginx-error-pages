# Custom nginx error pages

Original repo: https://github.com/denysvitali/nginx-error-pages

Customized version.

## Installation

On your server:

```
sudo mkdir -p /etc/nginx/error-pages
sudo git clone https://github.com/sebastiaanluca/nginx-error-pages.git /etc/nginx/error-pages

sudo mkdir -p /etc/nginx/snippets
sudo ln -nfs /etc/nginx/error-pages/snippets/error_pages.conf /etc/nginx/snippets/error_pages.conf
sudo ln -nfs /etc/nginx/error-pages/snippets/error_pages_content.conf /etc/nginx/snippets/error_pages_content.conf
```

Then include them in each of your virtual hosts config files:

```
# Enable custom error pages
include snippets/error_pages.conf;
```

## Screenshots

### 502 Error Page
![502 error page](screenshots/screenshot-1.png)

### 404 Error Page
![404 Error Page](screenshots/screenshot-2.png)

### 418 - I'm a Teapot
![418 Error Page](screenshots/screenshot-3.png)
