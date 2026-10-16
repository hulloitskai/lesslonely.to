# lesslonely.to

A static event calendar. Site files live in `www/`; no build step is required.

## Preview

Run `python3 -m http.server 8000 --directory www` and open http://localhost:8000.

## Publish

1. Push this project to a GitHub repository on the `main` branch.
2. In Settings → Pages, choose **GitHub Actions** as the source.
3. Set the custom domain to **lesslonely.to** in Settings → Pages. A custom workflow does not configure the domain from `CNAME` automatically.
4. Configure the domain's DNS for GitHub Pages, following [GitHub's custom domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).
5. Run the **Deploy GitHub Pages** workflow if it has not already run, and enable **Enforce HTTPS** once the certificate is available.

The workflow publishes only `www/`. Google Fonts and the Luma calendar require an internet connection; the calendar controls its own contents and scrolling.
