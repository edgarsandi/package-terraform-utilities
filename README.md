[![Maintained by Gruntwork.io](https://img.shields.io/badge/maintained%20by-gruntwork.io-%235849a6.svg)](https://gruntwork.io/?ref=repo_kubergrunt)

# Terraform Utility Modules

This repo contains miscellaneous utility and helper modules for use with Terraform.

## What is in this repo

This repo provides a Gruntwork IaC Package and has the following folder structure:

* [modules](/modules): This folder contains the main implementation code for this repository, broken down into multiple
  standalone modules.
* [examples](/examples): This folder contains examples of how to use the modules.
* [test](/test): Automated tests for the modules and examples.

The following modules are available:

* [intermediate-variable](/modules/intermediate-variable): A simple module that returns as output the exact variables
  you pass to it as inputs. This gives you a way to store intermediate values that contain interpolations.
* [join-path](/modules/join-path): This module can be used to join a list of given path parts into a single path that is
  platform/operating system aware.
* [operating-system](/modules/operating-system): This module can be used to figure out what operating system is being
  used to run Terraform.
* [require-executable](/modules/require-executable): This is a module that can be used to ensure particular executables
  is available in the `PATH`. **(This module requires Python)**
* [run-pex-as-data-source](/modules/run-pex-as-data-source): This module prepares a portable environment for running PEX
  files and runs them as an external data source. PEX files are python executables that contain all the requirements
  necessary to run the script. **(This module requires Python)**
* [run-pex-as-resource](/modules/run-pex-as-resource): This module prepares a portable environment for running PEX files
  and runs them as an local-exec provisioner on a null_resource. PEX files are python executables that contain all the
  requirements necessary to run the script. **(This module requires Python)**

Click on each module above to see its documentation. Head over to the [examples](/examples) folder for example usage.




## What is a module?

A Module is a canonical, reusable, best-practices definition for how to run a single piece of infrastructure, such as a
database or server cluster. Each Module is written using a combination of Terraform and scripts (mostly bash) and
include automated tests, documentation, and examples. It is maintained both by the open source community and companies
that provide commercial support.

Instead of figuring out the details of how to run a piece of infrastructure from scratch, you can reuse existing code
that has been proven in production. And instead of maintaining all that infrastructure code yourself, you can leverage
the work of the Module community to pick up infrastructure improvements through a version number bump.



## Who maintains this Module?

This Module is maintained by [Gruntwork](http://www.gruntwork.io/). If you're looking for help or commercial
support, send an email to [modules@gruntwork.io](mailto:modules@gruntwork.io?Subject=Terraform%20Utilities%20Module).
Gruntwork can help with:

* Setup, customization, and support for this Module.
* Modules for other types of infrastructure, such as VPCs, Docker clusters, databases, and continuous integration.
* Modules that meet compliance requirements, such as HIPAA.
* Consulting & Training on AWS, Terraform, and DevOps.




## How is this Module versioned?

This Module follows the principles of [Semantic Versioning](http://semver.org/). You can find each new release,
along with the changelog, in the [Releases Page](../../releases).

During initial development, the major version will be 0 (e.g., `0.x.y`), which indicates the code does not yet have a
stable API. Once we hit `1.0.0`, we will make every effort to maintain a backwards compatible API and use the MAJOR,
MINOR, and PATCH versions on each release to indicate any incompatibilities.





## License

Please see [LICENSE.txt](/LICENSE.txt) and [NOTICE](/NOTICE) for details on how the code in this repo is licensed.
