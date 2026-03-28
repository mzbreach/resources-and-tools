# umn-pages-template

Use this Template to quickly create a UMN Github Pages Site.

## Enable Github Actions and Dependabot

Remove the .tmpl file extension from `.github/dependabot.yml` and `.github/workflows/githubpages.yml`

* The `dependabot.yml` file will create pull requests to keep Actions up to date. [See our docs page to learn more about dependabot](https://github-docs.devex.oit.umn.edu/dependabot/) 

* The `githubpages.yml` file deploys a Github Pages site. The Action is configured to run on pushes to 'main' branch and will run on the [UMN Arc Runner](https://github-docs.devex.oit.umn.edu/action-runners/#self-hosted-runners).

Learn more about Github Actions [here](https://github-docs.devex.oit.umn.edu/actions/).

## Adjust mkdocs.yml

This github pages configuration uses [mkdocs](https://www.mkdocs.org/) to build the site.

There are several changes needed in the `mkdocs.yml` file. In the following example, replace any instance of the PLACEHOLDER items with your site's respective information. 

```yml
site_name: UMN PLACEHOLDER Docs
site_url: https://PLACEHOLDER.SUBDOMAIN.umn.edu/ # This will be used for your custom domain
site_description: >-
  PLACEHOLDER DESCRIPTION
# [...]
repo_url: https://github.com/YOUR_GITHUB_ORG/YOUR_SITE_NAME
repo_name: YOUR_SITE_NAME
```

## Populate `/docs/` directory with your docs

* `/docs/README.md` is the front page
* Every other `.md` file in the `/docs/` directory will be a page added to the left navigation bar (ex: `page-one.md`)
    * It uses the first H1 markdown header (ex: `# Page One`) as the title
    * If you want to create a submenu, you can create a directory in this folder and any pages that should be in that menu will go inside of that directory 
* `/stylesheets/color.css` file is configured to a UMN color scheme 
* `/imgs/` has UMN icons. This is also a good directory to put other images you wish to reference in your docs 
* `metadata.json` stores metadata information based on your mkdocs configuration 

## Configure Pages on github.com

* Build and deployment Source should be set to **GitHub Actions** 
    * Configuration for Github Pages is found in your repository settings tab in the `Code and Automation -> Pages` section 
* Set the appropriate visibility to your site
    * GitHub Pages visibility can be public (anyone on the internet) or private (anyone that has access to your repository) 

### Custom Domains

A custom domain will allow users to visit your site at a URL of `<sitename>.<dept>.umn.edu` instead of `fluffy-pjs.pages.github.io` (by default Github makes up a random name + `.github.io`).  Custom Domains are not required but nice. 

* University Relations has [design requirements](https://university-relations.umn.edu/resources/domains-and-branding) for any official University of Minnesota website (any sites using the apex domain `umn.edu`) 
* You will need a subdomain to use for your site -- if your department doesn't already have one, work with NTS to create one for your department 
    * For example, Devex's is `devex.oit.umn.edu` 

Email `nts-help@umn.edu` to open a ticket with the NTS team asking to **create a CNAME alias** for your custom subdomain to point to [your org's default domain](https://docs.github.com/en/enterprise-cloud@latest/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain); you can find this information on your repository's GitHub Pages Settings page. For example, Devex would submit a request for `test-docs.devex.oit.umn.edu` to be a CNAME alias for `umn-devex-test.github.io`. 

### Set up custom domain 

Once the records have been set-up, go back to the **Settings --> Pages** section and add your new URL to the Customer Domain section on the bottom of the page. Also, update the `site_name` in `mkdocs.yml`. Enforce HTTPS should be checked.
