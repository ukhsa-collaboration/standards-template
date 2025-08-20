# UKHSA Standards Template Repository

Welcome to the UKHSA standards template repository.
This is a template repository that can be used by teams at UKHSA to create their own standards documentation and have
them published on the [UKHSA Engineering Standards website][1].

## Purpose

The purpose of this repository is to provide a template teams can use to define their own technical standards related to
their area of work.
This repository is pre-configured with tools, configurations, and workflows to check that the documentation conforms to
the necessary standards to be published.

## Using this repository

1. Navigate to [this repository][2] on GitHub
1. Click the *"Use this template"* button to create a new repository.

Or, when creating a new repository on GitHub, choose this repository in the dropdown box next to the
*"Start with a repository"* option.

Once you have created a new repository from this template, you can then start adding documentation to the `docs/`
directory.

### Repository Setup

After creating a new repository based on this template, please undertake the following steps:

1. Replace the template specific parts of this readme file with suitable readme documentation for your new repository.
1. Rename `docs/your-standards.11tydata.json`, replacing the `your-standards` part with the name to be used when
   published.
1. Run `npm install` from the root of this repository to install the dev dependencies.

### Creating your documentation

All your documentation should be written in Markdown in the `docs/` directory.
The documentation is published using [Eleventy][3] along with the [UK Gov Eleventy Plugin][4] for styling.

A basic `index.md` is provided which can be modified to provide the index page for your documentation.
At present, the `your-standards.11tydata.json` file is also provided which sets some common [front matter][5] for the pages
of documentation so that they are displayed in a [sub-navigation layout][6].
Of course if you want to use a different layout, you can.

### Publishing your documentation

Contact a member of the [Org Standards Admins][7] team and they will add your repository to the [standards-org][8] repo.

## Local Publishing

To see how your docs look locally before publishing them you can use a container image:

```bash
docker run -p "8080:8080" -v "./docs:/site/docs/your-standards/" ghrc.io/ukhsa-collaboration/standards-org
```

*Replace `your-standards` with the path you'd like to expose your docs at.*

After running this command you can view your docs by going to [http://localhost:8080/your-standards/][9], again
replacing `your-standards` with the path you specified previously.
While this docker command is running it will notice when files change and update them so you can see how they look live.

## Contributing

We welcome contributions to improve these guidelines. Please read our [Contributing Guidelines][10] for
details on how to get involved.

## Licence

Unless stated otherwise, the codebase is released under [the MIT License][11].
This covers both the codebase and any sample code in the documentation.

The documentation is [© Crown copyright][12] and available under the terms
of the [Open Government 3.0][13] licence.

## Contact

TODO

[1]: https://ukhsa-collaboration.github.io/standards-org/
[2]: https://github.com/ukhsa-collaboration/standards-template
[3]: https://www.11ty.dev
[4]: https://github.com/x-govuk/govuk-eleventy-plugin
[5]: https://www.11ty.dev/docs/data-frontmatter/
[6]: https://x-govuk.github.io/govuk-eleventy-plugin/layouts/sub-navigation/
[7]: https://github.com/orgs/ukhsa-collaboration/teams/org-standards-admins
[8]: https://github.com/ukhsa-collaboration/standards-org
[9]: http://localhost:8080/your-standards/
[10]: CONTRIBUTING.md
[11]: LICENCE
[12]: https://www.nationalarchives.gov.uk/information-management/re-using-public-sector-information/uk-government-licensing-framework/crown-copyright/
[13]: https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/
