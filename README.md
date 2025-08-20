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
1. More?

### Creating your documentation

TODO

### Publishing your documentation

TODO

## Local Publishing

To see how your docs look locally before publishing them you can use a container image:

```bash
docker run -p "8080:8080" -v "./docs:/site/docs/your-standards" ukhsa-std-harness
```

*Replace `your-standards` with the path you'd like to expose your docs at.*

After running this command you can view your docs by going to [http://localhost:8080/your-standards/][3], again replacing
`your-standards` with the path you specified previously.
While this docker command is running it will notice when files change and update them so you can see how they look live.

## Contributing

We welcome contributions to improve these guidelines. Please read our [Contributing Guidelines][4] for
details on how to get involved.

## Licence

Unless stated otherwise, the codebase is released under [the MIT License][5].
This covers both the codebase and any sample code in the documentation.

The documentation is [© Crown copyright][6] and available under the terms
of the [Open Government 3.0][7] licence.

## Contact

TODO

[1]: https://ukhsa-collaboration.github.io/standards-org/
[2]: https://github.com/ukhsa-collaboration/standards-template
[3]: http://localhost:8080/your-standards/
[4]: CONTRIBUTING.md
[5]: LICENCE
[6]: https://www.nationalarchives.gov.uk/information-management/re-using-public-sector-information/uk-government-licensing-framework/crown-copyright/
[7]: https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/
