---
Title: syft
Homepage: https://github.com/anchore/syft
Repository: https://gitlab.com/kalilinux/packages/syft
Architectures: any
Version: 0.79.0+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### syft
 
  This package contains a CLI tool and Go library for generating a Software Bill
  of Materials (SBOM) from container images and filesystems. Exceptional for
  vulnerability detection when used with a scanner like Grype.
   
   * Generates SBOMs for container images, filesystems, archives, and more
     to discover packages and libraries
   * Supports OCI, Docker and Singularity image formats
   * Linux distribution identification
   * Works seamlessly with Grype (a fast, modern vulnerability scanner)
   * Able to create signed SBOM attestations using the in-toto
     specification
   * Convert between SBOM formats, such as CycloneDX, SPDX, and Syft's own
     format.
 
 **Installed size:** `33.42 MB`  
 **How to install:** `sudo apt install syft`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### syft
 
 
 ```
 root@kali:~# syft -h
 Generate a packaged-based Software Bill Of Materials (SBOM) from container images and filesystems
 
 Usage:
   syft [SOURCE] [flags]
   syft [command]
 
 Examples:
   syft packages alpine:latest                                a summary of discovered packages
   syft packages alpine:latest -o json                        show all possible cataloging details
   syft packages alpine:latest -o cyclonedx                   show a CycloneDX formatted SBOM
   syft packages alpine:latest -o cyclonedx-json              show a CycloneDX JSON formatted SBOM
   syft packages alpine:latest -o spdx                        show a SPDX 2.3 Tag-Value formatted SBOM
   syft packages alpine:latest -o spdx@2.2                    show a SPDX 2.2 Tag-Value formatted SBOM
   syft packages alpine:latest -o spdx-json                   show a SPDX 2.3 JSON formatted SBOM
   syft packages alpine:latest -o spdx-json@2.2               show a SPDX 2.2 JSON formatted SBOM
   syft packages alpine:latest -vv                            show verbose debug information
   syft packages alpine:latest -o template -t my_format.tmpl  show a SBOM formatted according to given template file
 
   Supports the following image sources:
     syft packages yourrepo/yourimage:tag     defaults to using images from a Docker daemon. If Docker is not present, the image is pulled directly from the registry.
     syft packages path/to/a/file/or/dir      a Docker tar, OCI tar, OCI directory, SIF container, or generic filesystem directory
 
   You can also explicitly specify the scheme to use:
     syft packages docker:yourrepo/yourimage:tag            explicitly use the Docker daemon
     syft packages podman:yourrepo/yourimage:tag            explicitly use the Podman daemon
     syft packages registry:yourrepo/yourimage:tag          pull image directly from a registry (no container runtime required)
     syft packages docker-archive:path/to/yourimage.tar     use a tarball from disk for archives created from "docker save"
     syft packages oci-archive:path/to/yourimage.tar        use a tarball from disk for OCI archives (from Skopeo or otherwise)
     syft packages oci-dir:path/to/yourimage                read directly from a path on disk for OCI layout directories (from Skopeo or otherwise)
     syft packages singularity:path/to/yourimage.sif        read directly from a Singularity Image Format (SIF) container on disk
     syft packages dir:path/to/yourproject                  read directly from a path on disk (any directory)
     syft packages file:path/to/yourproject/file            read directly from a path on disk (any single file)
 
 
 Available Commands:
   attest      Generate an SBOM as an attestation for the given [SOURCE] container image
   completion  Generate the autocompletion script for the specified shell
   convert     Convert between SBOM formats
   help        Help about any command
   login       Log in to a registry
   packages    Generate a package SBOM
   version     show the version
 
 Flags:
       --catalogers stringArray   enable one or more package catalogers
   -c, --config string            application config file
       --exclude stringArray      exclude paths from being scanned using a glob expression
       --file string              file to write the default report output to (default is STDOUT)
   -h, --help                     help for syft
       --name string              set the name of the target being analyzed
   -o, --output stringArray       report output format, options=[syft-json cyclonedx-xml cyclonedx-json github-json spdx-tag-value spdx-json syft-table syft-text template] (default [syft-table])
       --platform string          an optional platform specifier for container image sources (e.g. 'linux/arm64', 'linux/arm64/v8', 'arm64', 'linux')
   -q, --quiet                    suppress all logging output
   -s, --scope string             selection of layers to catalog, options=[Squashed AllLayers] (default "Squashed")
   -t, --template string          specify the path to a Go template file
   -v, --verbose count            increase verbosity (-v = info, -vv = debug)
       --version                  version for syft
 
 Use "syft [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
