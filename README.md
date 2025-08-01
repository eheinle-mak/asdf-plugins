# asdf plugins repository

The purpose of the [asdf](https://github.com/asdf-vm/asdf) plugins repository is to enable shorthand installation of plugins with:

```shell
asdf plugin add <name>
```

The asdf core team recommend using the long-form which does not rely on this repository:

```shell
asdf plugin add <name> <git_url>
```

Read each plugins code before installation and usage.

## Existing Plugins

Plugins listed here should be _stable_ and actively _maintained_. If you have issues with a specific plugin please raise them on the plugin repository first. If a deprecated plugin is listed here, please let us know and create a PR to add the most used alternative.

## Creating a new Plugin

- Read the [creating plugins guide](https://github.com/asdf-vm/asdf/blob/master/docs/plugins/create.md)
- Consider using our [Template](https://github.com/asdf-vm/asdf-plugin-template) which has the core functionality to tools published to GitHub releases and CI for GitHub/GitLab/CircleCI out of the box.

### `asdf-community`

If you're creating a new plugin consider creating it as part of the [`asdf-community`](https://github.com/asdf-community/.github) project. This is a separate community project with consolidated maintenance.

## Contributing a new Plugin

- Install repo dependencies: `asdf install`
- Add the plugin to the repository `README.md` _Plugin List_ table.
- Create a file with the shortname you wish to be used by asdf in `plugins/<name>`. The contents should be `repository = <your_repo>`.
  - eg: `printf "repository = https://github.com/asdf-vm/asdf-nodejs.git\n" > plugins/nodejs`
- Test your code : `scripts/test_plugin.bash --file plugins/<name>`
- Format your code & this README: `scripts/format.bash`
- Create a PR following the instructions in the PR template.

## Security

The `asdf` core provides a [security policy](https://github.com/asdf-vm/asdf/security/policy) which covers the core `asdf` tool. Plugins are the responsibility of their creators and not covered by the `asdf` policy. It is the responsibility of the user to evaluate each plugin they use for security concerns, even those in the `asdf-community` repositories. You can pin a plugin to a commit of the source repo with `asdf plugin update <name> <git-ref>`, however running `asdf plugin update <name>` or `asdf plugin update --all` will change the `sha` you have previously set.

## Plugin List

| Tool / Language               | Plugin Repository                                                                                                 |
| :---------------------------- | :---------------------------------------------------------------------------------------------------------------- |
| .Net                          | [hensou/asdf-dotnet](https://github.com/hensou/asdf-dotnet)                                                       |
| .Net Core                     | [emersonsoares/asdf-dotnet-core](https://github.com/emersonsoares/asdf-dotnet-core)                               |
| 1password-cli                 | [NeoHsu/asdf-1password-cli](https://github.com/NeoHsu/asdf-1password-cli)                                         |
| AAPT2                         | [ronnnnn/asdf-aapt2](https://github.com/ronnnnn/asdf-aapt2)                                                       |
| act                           | [gr1m0h/asdf-act](https://github.com/gr1m0h/asdf-act)                                                             |
| action-validator              | [mpalmer/action-validator](https://github.com/mpalmer/action-validator)                                           |
| actionlint                    | [crazy-matt/asdf-actionlint](https://github.com/crazy-matt/asdf-actionlint)                                       |
| adr-tools                     | [td7x/asdf/adr-tools](https://gitlab.com/td7x/asdf/adr-tools)                                                     |
| ag (the_silver_searcher)      | [koketani/asdf-ag](https://github.com/koketani/asdf-ag)                                                           |
| age                           | [threkk/asdf-age](https://github.com/threkk/asdf-age)                                                             |
| age-plugin-yubikey            | [str4d/asdf-age-plugin-yubikey](https://github.com/str4d/asdf-age-plugin-yubikey)                                 |
| agebox                        | [slok/asdf-agebox](https://github.com/slok/asdf-agebox)                                                           |
| air                           | [pdemagny/asdf-air](https://github.com/pdemagny/asdf-air)                                                         |
| aks-engine                    | [robsonpeixoto/asdf-aks-engine](https://github.com/robsonpeixoto/asdf-aks-engine)                                 |
| alias                         | [andrewthauer/asdf-alias](https://github.com/andrewthauer/asdf-alias)                                             |
| alire                         | [NyanHelsing/asdf-alire](https://github.com/NyanHelsing/asdf-alire)                                               |
| allure                        | [comdotlinux/asdf-allure](https://github.com/comdotlinux/asdf-allure)                                             |
| alp                           | [asdf-community/asdf-alp](https://github.com/asdf-community/asdf-alp)                                             |
| amass                         | [dhoeric/asdf-amass](https://github.com/dhoeric/asdf-amass)                                                       |
| Amazon ECR Credential Helper  | [dex4er/asdf-amazon-ecr-credential-helper](https://github.com/dex4er/asdf-amazon-ecr-credential-helper)           |
| Ambient                       | [jtakakura/asdf-ambient](https://github.com/jtakakura/asdf-ambient)                                               |
| Ansible (ansible-base)        | [amrox/asdf-pyapp](https://github.com/amrox/asdf-pyapp)                                                           |
| ant                           | [jackboespflug/asdf-ant](https://github.com/jackboespflug/asdf-ant)                                               |
| Apache Jmeter                 | [comdotlinux/asdf-jmeter](https://github.com/comdotlinux/asdf-jmeter)                                             |
| apko                          | [omissis/asdf-apko](https://github.com/omissis/asdf-apko)                                                         |
| apollo-ios-cli                | [MacPaw/asdf-apollo-ios-cli](https://github.com/MacPaw/asdf-apollo-ios-cli)                                       |
| Apollo Router                 | [safx/asdf-apollo-router](https://github.com/safx/asdf-apollo-router)                                             |
| arc                           | [ORCID/asdf-arc](https://github.com/ORCID/asdf-arc)                                                               |
| argc                          | [rgeraskin/asdf-argc](https://github.com/rgeraskin/asdf-argc)                                                     |
| argo                          | [sudermanjr/asdf-argo](https://github.com/sudermanjr/asdf-argo)                                                   |
| argo-rollouts                 | [abatilo/asdf-argo-rollouts](https://github.com/abatilo/asdf-argo-rollouts)                                       |
| argocd                        | [beardix/asdf-argocd](https://github.com/beardix/asdf-argocd)                                                     |
| argocd-image-updater          | [thatmlopsguy/asdf-argocd-image-updater](https://github.com/thatmlopsguy/asdf-argocd-image-updater)               |
| aria2                         | [asdf-community/asdf-aria2](https://github.com/asdf-community/asdf-aria2)                                         |
| asciidoctorj                  | [gliwka/asdf-asciidoctorj](https://github.com/gliwka/asdf-asciidoctorj)                                           |
| asdf-plugin-manager           | [asdf-community/asdf-plugin-manager](https://github.com/asdf-community/asdf-plugin-manager)                       |
| assh                          | [zekker6/asdf-assh](https://github.com/zekker6/asdf-assh)                                                         |
| atlas                         | [pbr0ck3r/asdf-atlas](https://github.com/pbr0ck3r/asdf-atlas)                                                     |
| atmos                         | [cloudposse/atmos](https://github.com/cloudposse/asdf-atmos)                                                      |
| auth0-cli                     | [gunzy83/asdf-auth0-cli](https://github.com/gunzy83/asdf-auth0-cli)                                               |
| auto-doc                      | [looztra/asdf-auto-doc](https://github.com/looztra/asdf-auto-doc)                                                 |
| avalanche                     | [embtools/asdf-avalanche](https://github.com/embtools/asdf-avalanche)                                             |
| avalanchego                   | [embtools/asdf-avalanchego](https://github.com/embtools/asdf-avalanchego)                                         |
| aws-copilot                   | [NeoHsu/asdf-copilot](https://github.com/NeoHsu/asdf-copilot)                                                     |
| aws-amplify-cli               | [LozanoMatheus/asdf-aws-amplify-cli](https://github.com/LozanoMatheus/asdf-aws-amplify-cli)                       |
| AWS IAM authenticator         | [zekker6/asdf-aws-iam-authenticator](https://github.com/zekker6/asdf-aws-iam-authenticator)                       |
| aws-nuke                      | [bersalazar/asdf-aws-nuke](https://github.com/bersalazar/asdf-aws-nuke)                                           |
| aws-sam-cli                   | [amrox/asdf-pyapp](https://github.com/amrox/asdf-pyapp)                                                           |
| aws-sso-cli                   | [adamcrews/asdf-aws-sso-cli](https://github.com/adamcrews/asdf-aws-sso-cli)                                       |
| awscli                        | [MetricMike/asdf-awscli](https://github.com/MetricMike/asdf-awscli)                                               |
| awscli-local                  | [paulo-ferraz-oliveira/asdf-awscli-local](https://github.com/paulo-ferraz-oliveira/asdf-awscli-local)             |
| awsebcli                      | [amrox/asdf-pyapp](https://github.com/amrox/asdf-pyapp)                                                           |
| aws-vault                     | [karancode/asdf-aws-vault](https://github.com/karancode/asdf-aws-vault)                                           |
| awsls                         | [chessmango/asdf-awsls](https://github.com/chessmango/asdf-awsls)                                                 |
| awsrm                         | [chessmango/asdf-awsrm](https://github.com/chessmango/asdf-awsrm)                                                 |
| awsweeper                     | [chessmango/asdf-awsweeper](https://github.com/chessmango/asdf-awsweeper)                                         |
| azure-cli (az)                | [EcoMind/asdf-azure-cli](https://github.com/EcoMind/asdf-azure-cli)                                               |
| Azure Functions Core Tools    | [daveneeley/asdf-azure-functions-core-tools](https://github.com/daveneeley/asdf-azure-functions-core-tools)       |
| babashka                      | [pitch-io/asdf-babashka](https://github.com/pitch-io/asdf-babashka)                                               |
| balena-cli                    | [boatkit-io/asdf-balena-cli](https://github.com/boatkit-io/asdf-balena-cli)                                       |
| bashbot                       | [mathew-fleisch/asdf-bashbot](https://github.com/mathew-fleisch/asdf-bashbot)                                     |
| bashly                        | [pcrockett/asdf-bashly](https://github.com/pcrockett/asdf-bashly)                                                 |
| bat                           | [pauloedurezende/asdf-bat](https://github.com/pauloedurezende/asdf-bat)                                           |
| bat-extras                    | [vhdirk/asdf-bat-extras](https://github.com/vhdirk/asdf-bat-extras)                                               |
| Batect                        | [johnlayton/asdf-batect](https://github.com/johnlayton/asdf-batect)                                               |
| Bats (Bash unittest)          | [timgluz/asdf-bats](https://github.com/timgluz/asdf-bats)                                                         |
| Bazel                         | [rajatvig/asdf-bazel](https://github.com/rajatvig/asdf-bazel)                                                     |
| bazelisk                      | [josephtate/asdf-bazelisk](https://github.com/josephtate/asdf-bazelisk)                                           |
| bbr                           | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| bbr-s3-config-validator       | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| benthos                       | [benthosdev/benthos-asdf](https://github.com/benthosdev/benthos-asdf)                                             |
| bfs                           | [virtualroot/asdf-bfs](https://github.com/virtualroot/asdf-bfs)                                                   |
| Binaryen                      | [cometkim/asdf-binaryen](https://github.com/cometkim/asdf-binaryen)                                               |
| bingo                         | [isindir/asdf-bingo](https://github.com/isindir/asdf-bingo)                                                       |
| binnacle                      | [Traackr/asdf-binnacle](https://github.com/Traackr/asdf-binnacle)                                                 |
| Bitwarden                     | [vixus0/asdf-bitwarden](https://github.com/vixus0/asdf-bitwarden)                                                 |
| bitwarden-secrets-manager     | [asdf-community/asdf-bitwarden-secrets-manager](https://github.com/asdf-community/asdf-bitwarden-secrets-manager) |
| boilerplate                   | [gruntwork-io/asdf-boilerplate](https://github.com/gruntwork-io/asdf-boilerplate)                                 |
| Bombardier                    | [NeoHsu/asdf-bombardier](https://github.com/NeoHsu/asdf-bombardier)                                               |
| borg                          | [lwiechec/asdf-borg](https://github.com/lwiechec/asdf-borg)                                                       |
| bosh                          | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| bottom (btm)                  | [carbonteq/asdf-btm](https://github.com/carbonteq/asdf-btm)                                                       |
| Boundary                      | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| bpkg                          | [bpkg/asdf-bpkg](https://github.com/bpkg/asdf-bpkg)                                                               |
| Brig                          | [Ibotta/asdf-brig](https://github.com/Ibotta/asdf-brig)                                                           |
| BTrace                        | [joschi/asdf-btrace](https://github.com/joschi/asdf-btrace)                                                       |
| Buf                           | [truepay/asdf-buf](https://github.com/truepay/asdf-buf)                                                           |
| Buildpack                     | [johnlayton/asdf-buildpack](https://github.com/johnlayton/asdf-buildpack)                                         |
| Bun                           | [cometkim/asdf-bun](https://github.com/cometkim/asdf-bun)                                                         |
| Bundler                       | [jonathanmorley/asdf-bundler](https://github.com/jonathanmorley/asdf-bundler)                                     |
| c3                            | [RobLoach/asdf-c3](https://github.com/RobLoach/asdf-c3)                                                           |
| Cabal                         | [sestrella/asdf-ghcup](https://github.com/sestrella/asdf-ghcup)                                                   |
| Caddy                         | [salasrod/asdf-caddy](https://github.com/salasrod/asdf-caddy)                                                     |
| cairo-coverage                | [software-mansion/asdf-cairo-coverage](https://github.com/software-mansion/asdf-cairo-coverage)                   |
| cairo-profiler                | [software-mansion/asdf-cairo-profiler](https://github.com/software-mansion/asdf-cairo-profiler)                   |
| CalendarSync                  | [FeryET/asdf-calendarsync](https://github.com/FeryET/asdf-calendarsync)                                           |
| calicoctl                     | [teejaded/asdf-calicoctl](https://github.com/teejaded/asdf-calicoctl)                                             |
| Camunda Modeler               | [barmac/asdf-camunda-modeler](https://github.com/barmac/asdf-camunda-modeler)                                     |
| cargo-make                    | [mise-plugins/asdf-cargo-make](https://github.com/mise-plugins/asdf-cargo-make)                                   |
| Carp                          | [susurri/asdf-carp](https://github.com/susurri/asdf-carp)                                                         |
| carthage                      | [younke/asdf-carthage](https://github.com/younke/asdf-carthage)                                                   |
| ccache                        | [asdf-community/asdf-ccache](https://github.com/asdf-community/asdf-ccache)                                       |
| certstrap                     | [carnei-ro/asdf-certstrap](https://github.com/carnei-ro/asdf-certstrap)                                           |
| cidr-merger                   | [ORCID/asdf-cidr-merger](https://github.com/ORCID/asdf-cidr-merger)                                               |
| cidrchk                       | [ORCID/asdf-cidrchk](https://github.com/ORCID/asdf-cidrchk)                                                       |
| circleci-cli                  | [ucpr/asdf-circleci-cli](https://github.com/ucpr/asdf-circleci-cli)                                               |
| cf                            | [mattysweeps/asdf-cf](https://github.com/mattysweeps/asdf-cf)                                                     |
| cfssl                         | [mathew-fleisch/asdf-cfssl](https://github.com/mathew-fleisch/asdf-cfssl)                                         |
| chamber                       | [mintel/asdf-chamber](https://github.com/mintel/asdf-chamber)                                                     |
| changie                       | [pdemagny/asdf-changie](https://github.com/pdemagny/asdf-changie)                                                 |
| cheat                         | [jmoratilla/asdf-cheat-plugin](https://github.com/jmoratilla/asdf-cheat-plugin)                                   |
| checkov                       | [bosmak/asdf-checkov](https://github.com/bosmak/asdf-checkov)                                                     |
| chezmoi                       | [joke/asdf-chezmoi](https://github.com/joke/asdf-chezmoi)                                                         |
| chezscheme                    | [asdf-community/asdf-chezscheme](https://github.com/asdf-community/asdf-chezscheme)                               |
| CHICKEN                       | [evhan/asdf-chicken](https://github.com/evhan/asdf-chicken)                                                       |
| chisel                        | [lwiechec/asdf-chisel](https://github.com/lwiechec/asdf-chisel)                                                   |
| choose                        | [carbonteq/asdf-choose](https://github.com/carbonteq/asdf-choose)                                                 |
| Chromedriver                  | [schinckel/asdf-chromedriver](https://github.com/schinckel/asdf-chromedriver)                                     |
| cilium-cli                    | [carnei-ro/asdf-cilium-cli](https://github.com/carnei-ro/asdf-cilium-cli)                                         |
| cilium-hubble                 | [NitriKx/asdf-cilium-hubble](https://github.com/NitriKx/asdf-cilium-hubble)                                       |
| Clarinet                      | [alexgo-io/asdf-clarinet](https://github.com/alexgo-io/asdf-clarinet)                                             |
| clj-kondo                     | [rynkowsg/asdf-clj-kondo](https://github.com/rynkowsg/asdf-clj-kondo)                                             |
| cljstyle                      | [abogoyavlensky/asdf-cljstyle](https://github.com/abogoyavlensky/asdf-cljstyle)                                   |
| Clojure                       | [asdf-community/asdf-clojure](https://github.com/asdf-community/asdf-clojure)                                     |
| Cloudflared                   | [threkk/asdf-cloudflared](https://github.com/threkk/asdf-cloudflared)                                             |
| cloud-sql-proxy               | [pbr0ck3r/asdf-cloud-sql-proxy](https://github.com/pbr0ck3r/asdf-cloud-sql-proxy)                                 |
| Clusterawsadm                 | [kahun/asdf-clusterawsadm](https://github.com/kahun/asdf-clusterawsadm)                                           |
| Clusterctl                    | [pfnet-research/asdf-clusterctl](https://github.com/pfnet-research/asdf-clusterctl)                               |
| cmctl                         | [asdf-community/asdf-cmctl](https://github.com/asdf-community/asdf-cmctl)                                         |
| CMake                         | [asdf-community/asdf-cmake](https://github.com/asdf-community/asdf-cmake)                                         |
| CockroachDB                   | [salasrod/asdf-cockroach](https://github.com/salasrod/asdf-cockroach)                                             |
| CocoaPods                     | [ronnnnn/asdf-cocoapods](https://github.com/ronnnnn/asdf-cocoapods)                                               |
| Codefresh                     | [gurukulkarni/asdf-codefresh](https://github.com/gurukulkarni/asdf-codefresh)                                     |
| CodeQL                        | [bored-engineer/asdf-codeql](https://github.com/bored-engineer/asdf-codeql)                                       |
| Colima                        | [CrouchingMuppet/asdf-colima](https://github.com/CrouchingMuppet/asdf-colima)                                     |
| coredns                       | [s3than/asdf-coredns](https://github.com/s3than/asdf-coredns)                                                     |
| Conan                         | [amrox/asdf-pyapp](https://github.com/amrox/asdf-pyapp)                                                           |
| Concourse                     | [mattysweeps/asdf-concourse](https://github.com/mattysweeps/asdf-concourse)                                       |
| Conduit                       | [gmcabrita/asdf-conduit](https://github.com/gmcabrita/asdf-conduit)                                               |
| Conform                       | [skyzyx/asdf-conform](https://github.com/skyzyx/asdf-conform)                                                     |
| conftest                      | [looztra/asdf-conftest](https://github.com/looztra/asdf-conftest)                                                 |
| Consul                        | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| container-diff                | [cgroschupp/asdf-container-diff](https://github.com/cgroschupp/asdf-container-diff)                               |
| container-structure-test      | [FeryET/asdf-container-structure-test](https://github.com/FeryET/asdf-container-structure-test)                   |
| cookiecutter                  | [shawon-crosen/asdf-cookiecutter](https://github.com/shawon-crosen/asdf-cookiecutter)                             |
| Copier                        | [looztra/asdf-copier](https://github.com/looztra/asdf-copier)                                                     |
| Copper                        | [vladlosev/asdf-copper](https://github.com/vladlosev/asdf-copper)                                                 |
| Coq                           | [gingerhot/asdf-coq](https://github.com/gingerhot/asdf-coq)                                                       |
| cosign                        | [wt0f/asdf-cosign](https://gitlab.com/wt0f/asdf-cosign)                                                           |
| coursier                      | [jiahuili430/asdf-coursier](https://github.com/jiahuili430/asdf-coursier)                                         |
| crane                         | [dmpe/asdf-crane](https://github.com/dmpe/asdf-crane)                                                             |
| crc                           | [sqtran/asdf-crc](https://github.com/sqtran/asdf-crc)                                                             |
| credhub                       | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| crictl                        | [FairwindsOps/asdf-crictl](https://github.com/FairwindsOps/asdf-crictl)                                           |
| crossplane-cli                | [joke/asdf-crossplane-cli](https://github.com/joke/asdf-crossplane-cli)                                           |
| ctlptl                        | [ezcater/asdf-ctlptl](https://github.com/ezcater/asdf-ctlptl)                                                     |
| Crystal                       | [asdf-community/asdf-crystal](https://github.com/asdf-community/asdf-crystal)                                     |
| ctop                          | [NeoHsu/asdf-ctop](https://github.com/NeoHsu/asdf-ctop)                                                           |
| CUE                           | [asdf-community/asdf-cue](https://github.com/asdf-community/asdf-cue)                                             |
| cyclonedx                     | [xeedio/asdf-cyclonedx](https://github.com/xeedio/asdf-cyclonedx)                                                 |
| D (DMD)                       | [sylph01/asdf-dmd](https://github.com/sylph01/asdf-dmd)                                                           |
| dagger                        | [virtualstaticvoid/asdf-dagger](https://github.com/virtualstaticvoid/asdf-dagger)                                 |
| dapr                          | [asdf-community/asdf-dapr-cli](https://github.com/asdf-community/asdf-dapr-cli.git)                               |
| Dart                          | [PatOConnor43/asdf-dart](https://github.com/PatOConnor43/asdf-dart)                                               |
| Dasel                         | [asdf-community/asdf-dasel](https://github.com/asdf-community/asdf-dasel)                                         |
| datree                        | [lukeab/asdf-datree](https://github.com/lukeab/asdf-datree)                                                       |
| Daytona                       | [CrouchingMuppet/asdf-daytona](https://github.com/CrouchingMuppet/asdf-daytona)                                   |
| Dbmate                        | [juusujanar/asdf-dbmate](https://github.com/juusujanar/asdf-dbmate)                                               |
| Deck                          | [nutellinoit/asdf-deck](https://github.com/nutellinoit/asdf-deck)                                                 |
| Delta                         | [andweeb/asdf-delta](https://github.com/andweeb/asdf-delta)                                                       |
| Deno                          | [asdf-community/asdf-deno](https://github.com/asdf-community/asdf-deno)                                           |
| Dep                           | [paxosglobal/asdf-dep](https://github.com/paxosglobal/asdf-dep)                                                   |
| depot                         | [depot/asdf-depot](https://github.com/depot/asdf-depot)                                                           |
| Desk                          | [endorama/asdf-desk](https://github.com/endorama/asdf-desk)                                                       |
| devpod-cli                    | [salemgolemugoo/asdf-devpod-cli](https://github.com/salemgolemugoo/asdf-devpod-cli)                               |
| DevSpace                      | [NeoHsu/asdf-devspace](https://github.com/NeoHsu/asdf-devspace)                                                   |
| DevStream                     | [zhenyuanlau/asdf-dtm](https://github.com/zhenyuanlau/asdf-dtm)                                                   |
| dhall                         | [aaaaninja/asdf-dhall](https://github.com/aaaaninja/asdf-dhall)                                                   |
| difftastic                    | [volf52/asdf-difftastic](https://github.com/volf52/asdf-difftastic)                                               |
| digdag                        | [jtakakura/asdf-digdag](https://github.com/jtakakura/asdf-digdag)                                                 |
| direnv                        | [asdf-community/asdf-direnv](https://github.com/asdf-community/asdf-direnv)                                       |
| dive                          | [looztra/asdf-dive](https://github.com/looztra/asdf-dive)                                                         |
| djinni                        | [cross-language-cpp/asdf-djinni](https://github.com/cross-language-cpp/asdf-djinni)                               |
| docker-slim                   | [xataz/asdf-docker-slim](https://github.com/xataz/asdf-docker-slim)                                               |
| docker-compose-v1             | [yilas/asdf-docker-compose-v1](https://github.com/yilas/asdf-docker-compose-v1)                                   |
| dockle                        | [mathew-fleisch/asdf-dockle](https://github.com/mathew-fleisch/asdf-dockle)                                       |
| doctl                         | [bstoutenburgh/asdf-doctl](https://github.com/bstoutenburgh/asdf-doctl)                                           |
| docToolchain                  | [joschi/asdf-doctoolchain](https://github.com/joschi/asdf-doctoolchain)                                           |
| docuum                        | [bradym/asdf-docuum](https://github.com/bradym/asdf-docuum)                                                       |
| dojo                          | [dojoengine/asdf-dojo](https://github.com/dojoengine/asdf-dojo)                                                   |
| DOME                          | [jtakakura/asdf-dome](https://github.com/jtakakura/asdf-dome)                                                     |
| doppler                       | [takutakahashi/asdf-doppler](https://github.com/takutakahashi/asdf-doppler)                                       |
| dotenv-linter                 | [wesleimp/asdf-dotenv-linter](https://github.com/wesleimp/asdf-dotenv-linter)                                     |
| dotenvx                       | [jgburet/asdf-dotenvx](https://github.com/jgburet/asdf-dotenvx)                                                   |
| Dotty                         | [asdf-community/asdf-dotty](https://github.com/asdf-community/asdf-dotty)                                         |
| dprint                        | [asdf-community/asdf-dprint](https://github.com/asdf-community/asdf-dprint)                                       |
| Draft                         | [kristoflemmens/asdf-draft](https://github.com/kristoflemmens/asdf-draft)                                         |
| Driftctl                      | [nlamirault/asdf-driftctl](https://github.com/nlamirault/asdf-driftctl)                                           |
| drone                         | [virtualstaticvoid/asdf-drone](https://github.com/virtualstaticvoid/asdf-drone)                                   |
| dst                           | [datasprayio/asdf-dst](https://github.com/datasprayio/asdf-dst)                                                   |
| dt                            | [so-dang-cool/asdf-dt](https://github.com/so-dang-cool/asdf-dt)                                                   |
| duf                           | [NeoHsu/asdf-duf](https://github.com/NeoHsu/asdf-duf)                                                             |
| dust                          | [looztra/asdf-dust](https://github.com/looztra/asdf-dust)                                                         |
| DVC                           | [fwfurtado/asdf-dvc](https://github.com/fwfurtado/asdf-dvc)                                                       |
| dyff                          | [wt0f/asdf-dyff](https://gitlab.com/wt0f/asdf-dyff)                                                               |
| dynatrace-monaco              | [nsaputro/asdf-monaco](https://github.com/nsaputro/asdf-monaco)                                                   |
| e1s                           | [tbobm/asdf-e1s](https://github.com/tbobm/asdf-e1s)                                                               |
| earthly                       | [YR-ZR0/asdf-earthly](https://github.com/YR-ZR0/asdf-earthly)                                                     |
| ecspresso                     | [kayac/asdf-ecspresso](https://github.com/kayac/asdf-ecspresso)                                                   |
| editorconfig-checker          | [gabitchov/asdf-editorconfig-checker](https://github.com/gabitchov/asdf-editorconfig-checker)                     |
| ejson                         | [cipherstash/asdf-ejson](https://github.com/cipherstash/asdf-ejson)                                               |
| eksctl                        | [elementalvoid/asdf-eksctl](https://github.com/elementalvoid/asdf-eksctl)                                         |
| eks-node-viewer               | [haad/asdf-eks-node-viewer](https://github.com/haad/asdf-eks-node-viewer)                                         |
| elixir-ls                     | [juantascon/asdf-elixir-ls](https://github.com/juantascon/asdf-elixir-ls)                                         |
| Elasticsearch                 | [asdf-community/asdf-elasticsearch](https://github.com/asdf-community/asdf-elasticsearch)                         |
| Elixir                        | [asdf-vm/asdf-elixir](https://github.com/asdf-vm/asdf-elixir)                                                     |
| Elm                           | [asdf-community/asdf-elm](https://github.com/asdf-community/asdf-elm)                                             |
| embulk                        | [yuokada/asdf-embulk](https://github.com/yuokada/asdf-embulk)                                                     |
| Emscripten SDK                | [RobLoach/asdf-emsdk](https://github.com/RobLoach/asdf-emsdk)                                                     |
| EnvCLI                        | [zekker6/asdf-envcli](https://github.com/zekker6/asdf-envcli)                                                     |
| envsubst                      | [dex4er/asdf-envsubst](https://github.com/dex4er/asdf-envsubst)                                                   |
| Ephemeral Postgres            | [smashedtoatoms/asdf-ephemeral-postgres](https://github.com/smashedtoatoms/asdf-ephemeral-postgres)               |
| Erlang                        | [asdf-vm/asdf-erlang](https://github.com/asdf-vm/asdf-erlang)                                                     |
| esc                           | [fxsalazar/asdf-esc](https://github.com/fxsalazar/asdf-esc)                                                       |
| esy                           | [asdf-community/asdf-esy](https://github.com/asdf-community/asdf-esy)                                             |
| etcd                          | [particledecay/asdf-etcd](https://github.com/particledecay/asdf-etcd)                                             |
| Evans                         | [goki90210/asdf-evans](https://github.com/goki90210/asdf-evans)                                                   |
| exa                           | [nyrst/asdf-exa](https://github.com/nyrst/asdf-exa)                                                               |
| exercism                      | [bheesham/asdf-exercism](https://gitlab.com/bheesham/asdf-exercism)                                               |
| eza                           | [lwiechec/asdf-eza](https://github.com/lwiechec/asdf-eza)                                                         |
| falco                         | [ronnnnn/asdf-falco](https://github.com/ronnnnn/asdf-falco)                                                       |
| fastlane                      | [mollyIV/asdf-fastlane](https://github.com/mollyIV/asdf-fastlane)                                                 |
| fd                            | [wt0f/asdf-fd](https://gitlab.com/wt0f/asdf-fd)                                                                   |
| ffizer                        | [ffizer/asdf-ffizer](https://github.com/ffizer/asdf-ffizer)                                                       |
| FFmpeg                        | [acj/asdf-ffmpeg](https://github.com/acj/asdf-ffmpeg)                                                             |
| figma-export                  | [younke/asdf-figma-export](https://github.com/younke/asdf-figma-export)                                           |
| fillin                        | [ouest/asdf-fillin](https://github.com/ouest/asdf-fillin)                                                         |
| firebase                      | [jthegedus/asdf-firebase](https://github.com/jthegedus/asdf-firebase)                                             |
| fission                       | [virtualstaticvoid/asdf-fission](https://github.com/virtualstaticvoid/asdf-fission)                               |
| Flamingo                      | [log2/asdf-flamingo](https://github.com/log2/asdf-flamingo)                                                       |
| flarectl                      | [ORCID/asdf-flarectl](https://github.com/ORCID/asdf-flarectl)                                                     |
| flatc                         | [TheOpenDictionary/asdf-flatc](https://github.com/TheOpenDictionary/asdf-flatc)                                   |
| Flutter                       | [oae/asdf-flutter](https://github.com/oae/asdf-flutter)                                                           |
| FlutterGen                    | [FlutterGen/asdf-fluttergen](https://github.com/FlutterGen/asdf-fluttergen)                                       |
| Flux2                         | [tablexi/asdf-flux2](https://github.com/tablexi/asdf-flux2)                                                       |
| Fluxctl                       | [stefansedich/asdf-fluxctl](https://github.com/stefansedich/asdf-fluxctl)                                         |
| fly                           | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| flyctl                        | [chessmango/asdf-flyctl](https://github.com/chessmango/asdf-flyctl)                                               |
| flyway                        | [junminahn/asdf-flyway](https://github.com/junminahn/asdf-flyway)                                                 |
| frankenphp                    | [theutz/asdf-frankenphp](https://github.com/theutz/asdf-frankenphp)                                               |
| func-e                        | [carnei-ro/asdf-func-e](https://github.com/carnei-ro/asdf-func-e)                                                 |
| Furyctl                       | [sighupio/asdf-furyctl](https://github.com/sighupio/asdf-furyctl)                                                 |
| fx                            | [wt0f/asdf-fx](https://gitlab.com/wt0f/asdf-fx)                                                                   |
| fzf                           | [kompiro/asdf-fzf](https://github.com/kompiro/asdf-fzf)                                                           |
| Gauche                        | [sakuro/asdf-gauche](https://github.com/sakuro/asdf-gauche)                                                       |
| gallery-dl                    | [iul1an/asdf-gallery-dl](https://github.com/iul1an/asdf-gallery-dl)                                               |
| gam                           | [offbyone/asdf-gam](https://github.com/offbyone/asdf-gam)                                                         |
| gator                         | [MxNxPx/asdf-gator](https://github.com/MxNxPx/asdf-gator)                                                         |
| garden-cli                    | [rynkowsg/asdf-garden-cli](https://github.com/rynkowsg/asdf-garden-cli)                                           |
| gcc-arm-none-eabi             | [dlech/asdf-gcc-arm-none-eabi](https://github.com/dlech/asdf-gcc-arm-none-eabi)                                   |
| gcloud                        | [jthegedus/asdf-gcloud](https://github.com/jthegedus/asdf-gcloud)                                                 |
| getenvoy                      | [asdf-community/asdf-getenvoy](https://github.com/asdf-community/asdf-getenvoy)                                   |
| GHC                           | [sestrella/asdf-ghcup](https://github.com/sestrella/asdf-ghcup)                                                   |
| ghidra                        | [Honeypot95/asdf-ghidra](https://github.com/Honeypot95/asdf-ghidra)                                               |
| ghorg                         | [gbloquel/asdf-ghorg](https://github.com/gbloquel/asdf-ghorg)                                                     |
| ghostty                       | [ilvez/asdf-ghostty](https://github.com/ilvez/asdf-ghostty)                                                       |
| ghq                           | [kajisha/asdf-ghq](https://github.com/kajisha/asdf-ghq)                                                           |
| ginkgo                        | [jimmidyson/asdf-ginkgo](https://github.com/jimmidyson/asdf-ginkgo)                                               |
| git                           | [jcaigitlab/asdf-git](https://gitlab.com/jcaigitlab/asdf-git)                                                     |
| git-chglog                    | [GoodwayGroup/asdf-git-chglog](https://github.com/GoodwayGroup/asdf-git-chglog)                                   |
| git-cliff                     | [jylenhof/asdf-git-cliff](https://github.com/jylenhof/asdf-git-cliff)                                             |
| git-lfs                       | [DanieleIsoni/asdf-git-lfs](https://github.com/DanieleIsoni/asdf-git-lfs)                                         |
| gitconfig                     | [0ghny/asdf-gitconfig](https://github.com/0ghny/asdf-gitconfig)                                                   |
| GitHub CLI                    | [bartlomiejdanek/asdf-github-cli](https://github.com/bartlomiejdanek/asdf-github-cli)                             |
| GitHub Markdown ToC           | [skyzyx/asdf-github-markdown-toc](https://github.com/skyzyx/asdf-github-markdown-toc)                             |
| Gitleaks                      | [jmcvetta/asdf-gitleaks](https://github.com/jmcvetta/asdf-gitleaks)                                               |
| Gitsign                       | [spencergilbert/asdf-gitsign](https://github.com/spencergilbert/asdf-gitsign)                                     |
| gitui                         | [looztra/asdf-gitui](https://github.com/looztra/asdf-gitui)                                                       |
| GLab                          | [particledecay/asdf-glab](https://github.com/particledecay/asdf-glab)                                             |
| Gleam                         | [vic/asdf-gleam](https://github.com/vic/asdf-gleam)                                                               |
| Glen                          | [bradym/asdf-glen](https://github.com/bradym/asdf-glen)                                                           |
| glooctl                       | [halilkaya/asdf-glooctl](https://github.com/halilkaya/asdf-glooctl)                                               |
| glow                          | [chessmango/asdf-glow](https://github.com/chessmango/asdf-glow)                                                   |
| GNU Guile                     | [indiebrain/asdf-guile](https://github.com/indiebrain/asdf-guile)                                                 |
| GNU nano                      | [mfakane/asdf-nano](https://github.com/mfakane/asdf-nano)                                                         |
| Go                            | [asdf-community/asdf-golang](https://github.com/asdf-community/asdf-golang)                                       |
| go-sdk                        | [yacchi/asdf-go-sdk](https://github.com/yacchi/asdf-go-sdk)                                                       |
| go-containerregistry          | [dex4er/asdf-go-containerregistry](https://github.com/dex4er/asdf-go-containerregistry)                           |
| go-getter                     | [ryodocx/asdf-go-getter](https://github.com/ryodocx/asdf-go-getter)                                               |
| go-jsonnet                    | [craigfurman/asdf-go-jsonnet](https://gitlab.com/craigfurman/asdf-go-jsonnet)                                     |
| go-jira                       | [dguihal/asdf-go-jira](https://github.com/dguihal/asdf-go-jira)                                                   |
| go-junit-report               | [jwillker/asdf-go-junit-report](https://github.com/jwillker/asdf-go-junit-report)                                 |
| go-swagger                    | [jfreeland/asdf-go-swagger](https://github.com/jfreeland/asdf-go-swagger)                                         |
| goconvey                      | [therounds-contrib/asdf-goconvey](https://github.com/therounds-contrib/asdf-goconvey)                             |
| gofumpt                       | [looztra/asdf-gofumpt](https://github.com/looztra/asdf-gofumpt)                                                   |
| GoHugo                        | [nklmilojevic/asdf-hugo](https://github.com/nklmilojevic/asdf-hugo)                                               |
| gobackup                      | [0ghny/asdf-gobackup](https://github.com/0ghny/asdf-gobackup)                                                     |
| gojq                          | [jimmidyson/asdf-gojq](https://github.com/jimmidyson/asdf-gojq)                                                   |
| golangci-lint                 | [hypnoglow/asdf-golangci-lint](https://github.com/hypnoglow/asdf-golangci-lint)                                   |
| Go Migrate                    | [joschi/asdf-gomigrate](https://github.com/joschi/asdf-gomigrate)                                                 |
| gomplate                      | [sneakybeaky/asdf-gomplate](https://github.com/sneakybeaky/asdf-gomplate)                                         |
| Gopass                        | [trallnag/asdf-gopass](https://github.com/trallnag/asdf-gopass)                                                   |
| GoReleaser                    | [kforsthoevel/asdf-goreleaser](https://github.com/kforsthoevel/asdf-goreleaser)                                   |
| Goss                          | [raimon49/asdf-goss](https://github.com/raimon49/asdf-goss)                                                       |
| GraalVM                       | [asdf-community/asdf-graalvm](https://github.com/asdf-community/asdf-graalvm)                                     |
| Gradle                        | [rfrancis/asdf-gradle](https://github.com/rfrancis/asdf-gradle)                                                   |
| Gradle Profiler               | [joschi/asdf-gradle-profiler](https://github.com/joschi/asdf-gradle-profiler)                                     |
| Grails                        | [weibemoura/asdf-grails](https://github.com/weibemoura/asdf-grails)                                               |
| Grain                         | [cometkim/asdf-grain](https://github.com/cometkim/asdf-grain)                                                     |
| Granted                       | [dex4er/asdf-granted](https://github.com/dex4er/asdf-granted)                                                     |
| grex                          | [ouest/asdf-grex](https://github.com/ouest/asdf-grex)                                                             |
| Groovy                        | [weibemoura/asdf-groovy](https://github.com/weibemoura/asdf-groovy)                                               |
| grpcurl                       | [asdf-community/asdf-grpcurl](https://github.com/asdf-community/asdf-grpcurl)                                     |
| grpc-health-probe             | [DanieleIsoni/asdf-grpc-health-probe](https://github.com/DanieleIsoni/asdf-grpc-health-probe)                     |
| grype                         | [poikilotherm/asdf-grype](https://github.com/poikilotherm/asdf-grype)                                             |
| gum                           | [lwiechec/asdf-gum](https://github.com/lwiechec/asdf-gum)                                                         |
| gwvault                       | [GoodwayGroup/asdf-gwvault](https://github.com/GoodwayGroup/asdf-gwvault)                                         |
| hadolint                      | [devlincashman/asdf-hadolint](https://github.com/devlincashman/asdf-hadolint)                                     |
| Hamler                        | [scudelletti/asdf-hamler](https://github.com/scudelletti/asdf-hamler)                                             |
| has                           | [sylvainmetayer/asdf-has](https://github.com/sylvainmetayer/asdf-has)                                             |
| Haskell                       | [asdf-community/asdf-haskell](https://github.com/asdf-community/asdf-haskell)                                     |
| Haskell Language Server (HLS) | [sestrella/asdf-ghcup](https://github.com/sestrella/asdf-ghcup)                                                   |
| Hasura-cli                    | [gurukulkarni/asdf-hasura](https://github.com/gurukulkarni/asdf-hasura)                                           |
| Haxe                          | [asdf-community/asdf-haxe](https://github.com/asdf-community/asdf-haxe)                                           |
| hcl2json                      | [dex4er/asdf-hcl2json](https://github.com/dex4er/asdf-hcl2json)                                                   |
| hcloud                        | [chessmango/asdf-hcloud](https://github.com/chessmango/asdf-hcloud)                                               |
| hcp                           | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| Helix Editor                  | [CSergienko/asdf-helix](https://github.com/CSergienko/asdf-helix)                                                 |
| Helm                          | [Antiarchitect/asdf-helm](https://github.com/Antiarchitect/asdf-helm)                                             |
| Helm Chart Releaser           | [Antiarchitect/asdf-helm-cr](https://github.com/Antiarchitect/asdf-helm-cr)                                       |
| Helm Chart Tester             | [tablexi/asdf-helm-ct](https://github.com/tablexi/asdf-helm-ct)                                                   |
| Helm Diff                     | [dex4er/asdf-helm-diff](https://github.com/dex4er/asdf-helm-diff)                                                 |
| helm-docs                     | [sudermanjr/asdf-helm-docs](https://github.com/sudermanjr/asdf-helm-docs)                                         |
| Helmfile                      | [feniix/asdf-helmfile](https://github.com/feniix/asdf-helmfile)                                                   |
| Helmsman                      | [luisdavim/asdf-helmsman](https://github.com/luisdavim/asdf-helmsman)                                             |
| Hermes                        | [cometkim/asdf-hermes](https://github.com/cometkim/asdf-hermes)                                                   |
| heroku-cli                    | [treilly94/asdf-heroku-cli](https://github.com/treilly94/asdf-heroku-cli)                                         |
| hey                           | [raimon49/asdf-hey](https://github.com/raimon49/asdf-hey)                                                         |
| hishtory                      | [asdf-community/asdf-hishtory](https://github.com/asdf-community/asdf-hishtory)                                   |
| hledger                       | [airtonix/hledger](https://github.com/airtonix/asdf-hledger)                                                      |
| hledger-flow                  | [airtonix/hledger-flow](https://github.com/airtonix/asdf-hledger-flow)                                            |
| hostctl                       | [svenluijten/asdf-hostctl](https://github.com/svenluijten/asdf-hostctl)                                           |
| httpie-go                     | [abatilo/asdf-httpie-go](https://github.com/abatilo/asdf-httpie-go)                                               |
| Hub                           | [claygorman/asdf-hub](https://github.com/claygorman/asdf-hub)                                                     |
| Hugo                          | [NeoHsu/asdf-hugo](https://github.com/NeoHsu/asdf-hugo)                                                           |
| Hurl                          | [raimon49/asdf-hurl](https://github.com/raimon49/asdf-hurl)                                                       |
| hwatch                        | [chessmango/asdf-hwatch](https://github.com/chessmango/asdf-hwatch)                                               |
| Hygen                         | [brentjanderson/asdf-hygen](https://github.com/brentjanderson/asdf-hygen)                                         |
| Hyperfine                     | [volf52/asdf-hyperfine](https://github.com/volf52/asdf-hyperfine)                                                 |
| iamlive                       | [chessmango/asdf-iamlive](https://github.com/chessmango/asdf-iamlive)                                             |
| iam-policy-json-to-terraform  | [carlduevel/asdf-iam-policy-json-to-terraform](https://github.com/carlduevel/asdf-iam-policy-json-to-terraform)   |
| IBLinter                      | [MaticConradi/asdf-iblinter](https://github.com/MaticConradi/asdf-iblinter)                                       |
| ibmcloud                      | [triangletodd/asdf-ibmcloud](https://github.com/triangletodd/asdf-ibmcloud)                                       |
| Idris                         | [asdf-community/asdf-idris](https://github.com/asdf-community/asdf-idris)                                         |
| Idris2                        | [asdf-community/asdf-idris2](https://github.com/asdf-community/asdf-idris2)                                       |
| ImageMagick                   | [mangalakader/asdf-imagemagick](https://github.com/mangalakader/asdf-imagemagick)                                 |
| imgpkg                        | [vmware-tanzu/asdf-carvel](https://github.com/vmware-tanzu/asdf-carvel)                                           |
| Infracost                     | [dex4er/asdf-infracost](https://github.com/dex4er/asdf-infracost)                                                 |
| Inlets                        | [nlamirault/asdf-inlets](https://github.com/nlamirault/asdf-inlets)                                               |
| Io                            | [mracos/asdf-io](https://github.com/mracos/asdf-io)                                                               |
| Istioctl                      | [virtualstaticvoid/asdf-istioctl](https://github.com/virtualstaticvoid/asdf-istioctl)                             |
| Janet                         | [Jakski/asdf-janet](https://github.com/Jakski/asdf-janet)                                                         |
| Java                          | [halcyon/asdf-java](https://github.com/halcyon/asdf-java)                                                         |
| jb                            | [beardix/asdf-jb](https://github.com/beardix/asdf-jb)                                                             |
| jbang                         | [jbangdev/jbang-asdf](https://github.com/jbangdev/jbang-asdf)                                                     |
| jet                           | [rynkowsg/asdf-jet](https://github.com/rynkowsg/asdf-jet)                                                         |
| jetbrains                     | [asdf-community/asdf-jetbrains](https://github.com/asdf-community/asdf-jetbrains)                                 |
| jfrog-cli                     | [LozanoMatheus/asdf-jfrog-cli](https://github.com/LozanoMatheus/asdf-jfrog-cli)                                   |
| jib                           | [joschi/asdf-jib](https://github.com/joschi/asdf-jib)                                                             |
| jiq                           | [chessmango/asdf-jiq](https://github.com/chessmango/asdf-jiq)                                                     |
| jless                         | [jc00ke/asdf-jless](https://github.com/jc00ke/asdf-jless)                                                         |
| JMESPath                      | [skyzyx/asdf-jmespath](https://github.com/skyzyx/asdf-jmespath)                                                   |
| jnv                           | [raimon49/asdf-jnv](https://github.com/raimon49/asdf-jnv)                                                         |
| jq                            | [lsanwick/asdf-jq](https://github.com/lsanwick/asdf-jq)                                                           |
| jqp                           | [wt0f/asdf-jqp](https://gitlab.com/wt0f/asdf-jqp)                                                                 |
| JReleaser                     | [joschi/asdf-jreleaser](https://github.com/joschi/asdf-jreleaser)                                                 |
| json2k8s                      | [k14s/asdf-k14s](https://github.com/k14s/asdf-k14s)                                                               |
| Jsonnet                       | [Banno/asdf-jsonnet](https://github.com/Banno/asdf-jsonnet)                                                       |
| Julia                         | [rkyleg/asdf-julia](https://github.com/rkyleg/asdf-julia)                                                         |
| Just                          | [olofvndrhr/asdf-just](https://github.com/olofvndrhr/asdf-just)                                                   |
| jx                            | [vbehar/asdf-jx](https://github.com/vbehar/asdf-jx)                                                               |
| k0sctl                        | [Its-Alex/asdf-plugin-k0sctl](https://github.com/Its-Alex/asdf-plugin-k0sctl)                                     |
| k2tf                          | [carlduevel/asdf-k2tf](https://github.com/carlduevel/asdf-k2tf)                                                   |
| k3d                           | [spencergilbert/asdf-k3d](https://github.com/spencergilbert/asdf-k3d)                                             |
| k3kcli                        | [xanmanning/asdf-k3kcli](https://github.com/xanmanning/asdf-k3kcli)                                               |
| k3s                           | [dmpe/asdf-k3s](https://github.com/dmpe/asdf-k3s)                                                                 |
| k3sup                         | [cgroschupp/asdf-k3sup](https://github.com/cgroschupp/asdf-k3sup)                                                 |
| k6                            | [gr1m0h/asdf-k6](https://github.com/gr1m0h/asdf-k6)                                                               |
| k9s                           | [looztra/asdf-k9s](https://github.com/looztra/asdf-k9s)                                                           |
| kafka                         | [ueisele/asdf-kafka](https://github.com/ueisele/asdf-kafka)                                                       |
| kafkactl                      | [anweber/asdf-kafkactl](https://github.com/anweber/asdf-kafkactl)                                                 |
| kapp                          | [vmware-tanzu/asdf-carvel](https://github.com/vmware-tanzu/asdf-carvel)                                           |
| kbld                          | [vmware-tanzu/asdf-carvel](https://github.com/vmware-tanzu/asdf-carvel)                                           |
| kcat                          | [douglasdgoulart/asdf-kcat](https://github.com/douglasdgoulart/asdf-kcat)                                         |
| kcctl                         | [joschi/asdf-kcctl](https://github.com/joschi/asdf-kcctl)                                                         |
| kcl                           | [starkers/asdf-kcl](https://github.com/starkers/asdf-kcl)                                                         |
| kconf                         | [particledecay/asdf-kconf](https://github.com/particledecay/asdf-kconf)                                           |
| Kind                          | [johnlayton/asdf-kind](https://github.com/johnlayton/asdf-kind)                                                   |
| Kiota                         | [asdf-community/asdf-kiota](https://github.com/asdf-community/asdf-kiota)                                         |
| ki                            | [comdotlinux/asdf-ki](https://github.com/comdotlinux/asdf-ki)                                                     |
| kn                            | [joke/asdf-kn](https://github.com/joke/asdf-kn)                                                                   |
| ko                            | [zasdaym/asdf-ko](https://github.com/zasdaym/asdf-ko)                                                             |
| Koka                          | [susurri/asdf-koka](https://github.com/susurri/asdf-koka)                                                         |
| Kompose                       | [technikhil314/asdf-kompose](https://github.com/technikhil314/asdf-kompose)                                       |
| konstraint                    | [tapih/asdf-konstraint](https://github.com/tapih/asdf-konstraint)                                                 |
| Kops                          | [Antiarchitect/asdf-kops](https://github.com/Antiarchitect/asdf-kops)                                             |
| Kotlin                        | [asdf-community/asdf-kotlin](https://github.com/asdf-community/asdf-kotlin)                                       |
| Kpt                           | [nlamirault/asdf-kpt](https://github.com/nlamirault/asdf-kpt)                                                     |
| kp                            | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| kpack                         | [asdf-community/asdf-kpack-cli](https://github.com/asdf-community/asdf-kpack-cli)                                 |
| kscript                       | [edgelevel/asdf-kscript](https://github.com/edgelevel/asdf-kscript)                                               |
| krab                          | [ohkrab/asdf-krab](https://github.com/ohkrab/asdf-krab)                                                           |
| krelay                        | [asdf-community/asdf-krelay](https://github.com/asdf-community/asdf-krelay)                                       |
| krew                          | [bjw-s/asdf-krew](https://github.com/bjw-s/asdf-krew)                                                             |
| Ksonnet                       | [Banno/asdf-ksonnet](https://github.com/Banno/asdf-ksonnet)                                                       |
| ksops                         | [janpieper/asdf-ksops](https://github.com/janpieper/asdf-ksops)                                                   |
| ktlint                        | [esensar/asdf-ktlint](https://github.com/esensar/asdf-ktlint)                                                     |
| kube-capacity                 | [looztra/asdf-kube-capacity](https://github.com/looztra/asdf-kube-capacity)                                       |
| kube-code-generator           | [jimmidyson/asdf-kube-code-generator](https://github.com/jimmidyson/asdf-kube-code-generator)                     |
| kube-controller-tools         | [jimmidyson/asdf-kube-controller-tools](https://github.com/jimmidyson/asdf-kube-controller-tools)                 |
| kube-credential-cache         | [ryodocx/kube-credential-cache](https://github.com/ryodocx/kube-credential-cache)                                 |
| kube-linter                   | [devlincashman/asdf-kube-linter](https://github.com/devlincashman/asdf-kube-linter)                               |
| kube-score                    | [bageljp/asdf-kube-score](https://github.com/bageljp/asdf-kube-score)                                             |
| kubebuilder                   | [virtualstaticvoid/asdf-kubebuilder](https://github.com/virtualstaticvoid/asdf-kubebuilder)                       |
| kubecm                        | [samhvw8/asdf-kubecm](https://github.com/samhvw8/asdf-kubecm)                                                     |
| kubecolor                     | [dex4er/asdf-kubecolor](https://github.com/dex4er/asdf-kubecolor)                                                 |
| kubeconform                   | [lirlia/asdf-kubeconform](https://github.com/lirlia/asdf-kubeconform)                                             |
| Kubectl                       | [asdf-community/asdf-kubectl](https://github.com/asdf-community/asdf-kubectl)                                     |
| kubectl-bindrole              | [looztra/asdf-kubectl-bindrole](https://github.com/looztra/asdf-kubectl-bindrole)                                 |
| kubectl-convert               | [iul1an/asdf-kubectl-convert](https://github.com/iul1an/asdf-kubectl-convert)                                     |
| kubectl-kots                  | [ganta/asdf-kubectl-kots](https://github.com/ganta/asdf-kubectl-kots)                                             |
| kubectl-oidc_login            | [ezcater/asdf-kubectl-oidc_login](https://github.com/ezcater/asdf-kubectl-oidc_login)                             |
| kubectx                       | [wt0f/asdf-kubectx](https://gitlab.com/wt0f/asdf-kubectx)                                                         |
| Kubefedctl                    | [kvokka/asdf-kubefedctl](https://github.com/kvokka/asdf-kubefedctl)                                               |
| Kubefirst                     | [Claywd/asdf-kubefirst](https://github.com/Claywd/asdf-kubefirst)                                                 |
| Kubelogin                     | [sechmann/asdf-kubelogin](https://github.com/sechmann/asdf-kubelogin)                                             |
| Kubemqctl                     | [johnlayton/asdf-kubemqctl](https://github.com/johnlayton/asdf-kubemqctl)                                         |
| kubent                        | [virtualstaticvoid/asdf-kubent](https://github.com/virtualstaticvoid/asdf-kubent)                                 |
| kubeone                       | [PandaScience/asdf-kubeone](https://github.com/PandaScience/asdf-kubeone)                                         |
| Kubergrunt                    | [NeoHsu/asdf-kubergrunt](https://github.com/NeoHsu/asdf-kubergrunt)                                               |
| Kubeseal                      | [stefansedich/asdf-kubeseal](https://github.com/stefansedich/asdf-kubeseal)                                       |
| Kubesec                       | [vitalis/asdf-kubesec](https://github.com/vitalis/asdf-kubesec)                                                   |
| kubeshark                     | [carnei-ro/asdf-kubeshark](https://github.com/carnei-ro/asdf-kubeshark)                                           |
| kubespy                       | [jfreeland/asdf-kubespy](https://github.com/jfreeland/asdf-kubespy)                                               |
| Kubeval                       | [stefansedich/asdf-kubeval](https://github.com/stefansedich/asdf-kubeval)                                         |
| KubeVela                      | [gustavclausen/asdf-kubevela](https://github.com/gustavclausen/asdf-kubevela)                                     |
| Kubie                         | [johnhamelink/asdf-kubie](https://github.com/johnhamelink/asdf-kubie)                                             |
| Kustomize                     | [Banno/asdf-kustomize](https://github.com/Banno/asdf-kustomize)                                                   |
| kuttl                         | [jimmidyson/asdf-kuttl](https://github.com/jimmidyson/asdf-kuttl)                                                 |
| kwt                           | [vmware-tanzu/asdf-carvel](https://github.com/vmware-tanzu/asdf-carvel)                                           |
| lab                           | [particledecay/asdf-lab](https://github.com/particledecay/asdf-lab)                                               |
| lane                          | [CodeReaper/asdf-lane](https://github.com/CodeReaper/asdf-lane)                                                   |
| launchpad                     | [surskitt/asdf-launchpad](https://github.com/surskitt/asdf-launchpad)                                             |
| lazygit                       | [nklmilojevic/asdf-lazygit](https://github.com/nklmilojevic/asdf-lazygit)                                         |
| Lean                          | [asdf-community/asdf-lean](https://github.com/asdf-community/asdf-lean)                                           |
| Leiningen                     | [miorimmax/asdf-lein](https://github.com/miorimmax/asdf-lein)                                                     |
| Lefthook                      | [jtzero/asdf-lefthook](https://github.com/jtzero/asdf-lefthook)                                                   |
| Levant                        | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| LFE                           | [asdf-community/asdf-lfe](https://github.com/asdf-community/asdf-lfe)                                             |
| libsql-server                 | [jonasb/asdf-libsql-server](https://github.com/jonasb/asdf-libsql-server)                                         |
| Lima                          | [CrouchingMuppet/asdf-lima](https://github.com/CrouchingMuppet/asdf-lima)                                         |
| Link (system tools)           | [asdf-community/asdf-link](https://github.com/asdf-community/asdf-link)                                           |
| Linkerd                       | [kforsthoevel/asdf-linkerd](https://github.com/kforsthoevel/asdf-linkerd)                                         |
| liqoctl                       | [pdemagny/asdf-liqoctl](https://github.com/pdemagny/asdf-liqoctl)                                                 |
| liquibase                     | [saliougaye/asdf-liquibase](https://github.com/saliougaye/asdf-liquibase)                                         |
| Litestream                    | [threkk/asdf-litestream](https://github.com/threkk/asdf-litestream)                                               |
| Logtalk                       | [LogtalkDotOrg/asdf-logtalk](https://github.com/LogtalkDotOrg/asdf-logtalk)                                       |
| Loki-Logcli                   | [comdotlinux/asdf-loki-logcli](https://github.com/comdotlinux/asdf-loki-logcli)                                   |
| lq                            | [jylenhof/asdf-lq](https://github.com/jylenhof/asdf-lq)                                                           |
| ls-lint                       | [ameausoone/asdf-ls-lint](https://github.com/ameausoone/asdf-ls-lint)                                             |
| Lua                           | [Stratus3D/asdf-lua](https://github.com/Stratus3D/asdf-lua)                                                       |
| LuaJIT                        | [smashedtoatoms/asdf-luaJIT](https://github.com/smashedtoatoms/asdf-luaJIT)                                       |
| lua-language-server           | [bellini666/asdf-lua-language-server](https://github.com/bellini666/asdf-lua-language-server)                     |
| Lucy                          | [cometkim/asdf-lucy](https://github.com/cometkim/asdf-lucy)                                                       |
| maestro                       | [dotanuki-labs/asdf-maestro](https://github.com/dotanuki-labs/asdf-maestro)                                       |
| mage                          | [mathew-fleisch/asdf-mage](https://github.com/mathew-fleisch/asdf-mage)                                           |
| make                          | [yacchi/asdf-make](https://github.com/yacchi/asdf-make)                                                           |
| mani                          | [anweber/asdf-mani](https://github.com/anweber/asdf-mani)                                                         |
| mark                          | [jfreeland/asdf-mark](https://github.com/jfreeland/asdf-mark)                                                     |
| markdownlint-cli2             | [paulo-ferraz-oliveira/asdf-markdownlint-cli2](https://github.com/paulo-ferraz-oliveira/asdf-markdownlint-cli2)   |
| marp-cli                      | [xataz/asdf-marp-cli](https://github.com/xataz/asdf-marp-cli)                                                     |
| mask                          | [aaaaninja/asdf-mask](https://github.com/aaaaninja/asdf-mask)                                                     |
| Maven                         | [halcyon/asdf-maven](https://github.com/halcyon/asdf-maven)                                                       |
| mdbook                        | [hashemi-soroush/asdf-mdbook](https://github.com/hashemi-soroush/asdf-mdbook)                                     |
| mdbook-linkcheck              | [cipherstash/asdf-mdbook-linkcheck](https://github.com/cipherstash/asdf-mdbook-linkcheck)                         |
| melange                       | [omissis/asdf-melange](https://github.com/omissis/asdf-melange)                                                   |
| melt                          | [chessmango/asdf-melt](https://github.com/chessmango/asdf-melt)                                                   |
| Memcached                     | [furkanural/asdf-memcached](https://github.com/furkanural/asdf-memcached)                                         |
| Mercury                       | [susurri/asdf-mercury](https://github.com/susurri/asdf-mercury)                                                   |
| Meson                         | [asdf-community/asdf-meson](https://github.com/asdf-community/asdf-meson)                                         |
| Micronaut                     | [xafarr/asdf-micronaut](https://github.com/xafarr/asdf-micronaut)                                                 |
| Mill                          | [asdf-community/asdf-mill](https://github.com/asdf-community/asdf-mill)                                           |
| mimirtool                     | [asdf-community/asdf-mimirtool](https://github.com/asdf-community/asdf-mimirtool)                                 |
| minify                        | [axilleas/asdf-minify](https://github.com/axilleas/asdf-minify)                                                   |
| Minikube                      | [alvarobp/asdf-minikube](https://github.com/alvarobp/asdf-minikube)                                               |
| Minio                         | [aeons/asdf-minio](https://github.com/aeons/asdf-minio)                                                           |
| Minio Client                  | [penpyt/asdf-mc](https://github.com/penpyt/asdf-mc)                                                               |
| Minishift                     | [sqtran/asdf-minishift](https://github.com/sqtran/asdf-minishift)                                                 |
| Mint                          | [mint-lang/asdf-mint](https://github.com/mint-lang/asdf-mint)                                                     |
| mirrord                       | [metalbear-co/asdf-mirrord](https://github.com/metalbear-co/asdf-mirrord)                                         |
| mitmproxy                     | [NeoHsu/asdf-mitmproxy](https://github.com/NeoHsu/asdf-mitmproxy)                                                 |
| mkcert                        | [salasrod/asdf-mkcert](https://github.com/salasrod/asdf-mkcert)                                                   |
| mlton                         | [asdf-community/asdf-mlton](https://github.com/asdf-community/asdf-mlton)                                         |
| mockery                       | [cabify/asdf-mockery](https://github.com/cabify/asdf-mockery)                                                     |
| mockolo                       | [MontakOleg/asdf-mockolo](https://github.com/MontakOleg/asdf-mockolo)                                             |
| Monarch                       | [nyuyuyu/asdf-monarch](https://github.com/nyuyuyu/asdf-monarch)                                                   |
| mongo-tools                   | [itspngu/asdf-mongo-tools](https://github.com/itspngu/asdf-mongo-tools)                                           |
| MongoDB                       | [sylph01/asdf-mongodb](https://github.com/sylph01/asdf-mongodb)                                                   |
| mongodb-database-tools        | [egose/database-tools](https://github.com/egose/asdf-database-tools)                                              |
| mongosh                       | [itspngu/asdf-mongosh](https://github.com/itspngu/asdf-mongosh)                                                   |
| mutanus                       | [SoriUR/asdf-mutanus](https://github.com/SoriUR/asdf-mutanus)                                                     |
| mvnd                          | [joschi/asdf-mvnd](https://github.com/joschi/asdf-mvnd)                                                           |
| MySQL                         | [iroddis/asdf-mysql](https://github.com/iroddis/asdf-mysql)                                                       |
| nancy                         | [iilyak/asdf-nancy](https://github.com/iilyak/asdf-nancy)                                                         |
| nasm                          | [Dpbm/asdf-nasm](https://github.com/Dpbm/asdf-nasm)                                                               |
| Neko Virtual Machine          | [asdf-community/asdf-neko](https://github.com/asdf-community/asdf-neko)                                           |
| Neovim                        | [richin13/asdf-neovim](https://github.com/richin13/asdf-neovim)                                                   |
| Nerves Toolchain              | [nerves-project/asdf-plugin-nerves-toolchain](https://github.com/nerves-project/asdf-plugin-nerves-toolchain)     |
| nerdctl                       | [dmpe/asdf-nerdctl](https://github.com/dmpe/asdf-nerdctl)                                                         |
| newrelic-cli                  | [NeoHsu/asdf-newrelic-cli](https://github.com/NeoHsu/asdf-newrelic-cli)                                           |
| nfpm                          | [ORCID/asdf-nfpm](https://github.com/ORCID/asdf-nfpm)                                                             |
| Nim                           | [asdf-community/asdf-nim](https://github.com/asdf-community/asdf-nim)                                             |
| Ninja                         | [asdf-community/asdf-ninja](https://github.com/asdf-community/asdf-ninja)                                         |
| Node.js                       | [asdf-vm/asdf-nodejs](https://github.com/asdf-vm/asdf-nodejs)                                                     |
| Nomad                         | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| nomad-pack                    | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| notation                      | [bodgit/asdf-notation](https://github.com/bodgit/asdf-notation)                                                   |
| nova                          | [elementalvoid/asdf-nova](https://github.com/elementalvoid/asdf-nova)                                             |
| NSC                           | [dex4er/asdf-nsc](https://github.com/dex4er/asdf-nsc)                                                             |
| oapi-codegen                  | [dylanrayboss/asdf-oapi-codegen](https://github.com/dylanrayboss/asdf-oapi-codegen)                               |
| oc                            | [sqtran/asdf-oc](https://github.com/sqtran/asdf-oc)                                                               |
| oci                           | [yasn77/asdf-oci](https://github.com/yasn77/asdf-oci)                                                             |
| OCaml                         | [asdf-community/asdf-ocaml](https://github.com/asdf-community/asdf-ocaml)                                         |
| Odin                          | [jtakakura/asdf-odin](https://github.com/jtakakura/asdf-odin)                                                     |
| odo                           | [rm3l/asdf-odo](https://github.com/rm3l/asdf-odo)                                                                 |
| okta-aws-cli                  | [bennythejudge/asdf-plugin-okta-aws-cli](https://github.com/bennythejudge/asdf-plugin-okta-aws-cli)               |
| Okteto                        | [BradenM/asdf-okteto](https://github.com/BradenM/asdf-okteto)                                                     |
| ollama                        | [virtualstaticvoid/asdf-ollama](https://github.com/virtualstaticvoid/asdf-ollama)                                 |
| om                            | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| Onyx                          | [jtakakura/asdf-onyx](https://github.com/jtakakura/asdf-onyx)                                                     |
| OPA                           | [tochukwuvictor/asdf-opa](https://github.com/tochukwuvictor/asdf-opa)                                             |
| Opam                          | [asdf-community/asdf-opam](https://github.com/asdf-community/asdf-opam)                                           |
| openfaas-faas-cli             | [zekker6/asdf-faas-cli](https://github.com/zekker6/asdf-faas-cli)                                                 |
| OpenResty                     | [smashedtoatoms/asdf-openresty](https://github.com/smashedtoatoms/asdf-openresty)                                 |
| opensearch                    | [randikabanura/asdf-opensearch](https://github.com/randikabanura/asdf-opensearch)                                 |
| opensearch-cli                | [iul1an/asdf-opensearch-cli](https://github.com/iul1an/asdf-opensearch-cli)                                       |
| openshift-install             | [hhemied/asdf-openshift-install](https://github.com/hhemied/asdf-openshift-install)                               |
| opentofu                      | [virtualroot/asdf-opentofu](https://github.com/virtualroot/asdf-opentofu)                                         |
| Operator SDK                  | [Medium/asdf-operator-sdk](https://github.com/Medium/asdf-operator-sdk)                                           |
| Opsgenie-lamp                 | [ORCID/asdf-opsgenie-lamp](https://github.com/ORCID/asdf-opsgenie-lamp)                                           |
| oras                          | [bodgit/asdf-oras](https://github.com/bodgit/asdf-oras)                                                           |
| Osm                           | [nlamirault/asdf-osm](https://github.com/nlamirault/asdf-osm)                                                     |
| osqueryi                      | [davidecavestro/asdf-osqueryi](https://github.com/davidecavestro/asdf-osqueryi)                                   |
| pachctl                       | [abatilo/asdf-pachctl](https://github.com/abatilo/asdf-pachctl)                                                   |
| Packer                        | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| Pandoc                        | [Fbrisset/asdf-pandoc](https://github.com/Fbrisset/asdf-pandoc)                                                   |
| pandoc-crossref               | [sys9kdr/asdf-pandoc-crossref](https://github.com/sys9kdr/asdf-pandoc-crossref)                                   |
| patat                         | [airtonix/asdf-patat](https://github.com/airtonix/asdf-patat)                                                     |
| peco                          | [asdf-community/asdf-peco](https://github.com/asdf-community/asdf-peco)                                           |
| pdm                           | [1oglop1/asdf-pdm](https://github.com/1oglop1/asdf-pdm)                                                           |
| Perl                          | [ouest/asdf-perl](https://github.com/ouest/asdf-perl)                                                             |
| PHP                           | [asdf-community/asdf-php](https://github.com/asdf-community/asdf-php)                                             |
| Phrase                        | [bitfrost/asdf-phrase](https://github.com/bitfrost/asdf-phrase)                                                   |
| pint                          | [sam-burrell/asdf-pint](https://github.com/sam-burrell/asdf-pint)                                                 |
| pipectl                       | [pipe-cd/asdf-pipectl](https://github.com/pipe-cd/asdf-pipectl)                                                   |
| pipelight                     | [kogeletey/asdf-pipelight](https://github.com/kogeletey/asdf-pipelight)                                           |
| pipx                          | [yozachar/asdf-pipx](https://github.com/yozachar/asdf-pipx)                                                       |
| pivnet                        | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| pixi                          | [pavelzw/pixi](https://github.com/pavelzw/asdf-pixi)                                                              |
| pkl                           | [mise-plugins/asdf-pkl](https://github.com/mise-plugins/asdf-pkl)                                                 |
| PlantScale CLI                | [kota65535/asdf-planetscale-cli](https://github.com/kota65535/asdf-planetscale-cli)                               |
| Please                        | [asdf-community/asdf-please](https://github.com/asdf-community/asdf-please)                                       |
| Pluto                         | [FairwindsOps/asdf-pluto](https://github.com/FairwindsOps/asdf-pluto)                                             |
| pnpm                          | [jonathanmorley/asdf-pnpm](https://github.com/jonathanmorley/asdf-pnpm)                                           |
| Poetry                        | [asdf-community/asdf-poetry](https://github.com/asdf-community/asdf-poetry)                                       |
| Polaris                       | [particledecay/asdf-polaris](https://github.com/particledecay/asdf-polaris)                                       |
| Popeye                        | [nlamirault/asdf-popeye](https://github.com/nlamirault/asdf-popeye)                                               |
| Postgres                      | [smashedtoatoms/asdf-postgres](https://github.com/smashedtoatoms/asdf-postgres)                                   |
| powerpipe                     | [vmdude/asdf-powerpipe](https://github.com/vmdude/asdf-powerpipe)                                                 |
| powerline-go                  | [dex4er/asdf-powerline-go](https://github.com/dex4er/asdf-powerline-go)                                           |
| PowerShell                    | [daveneeley/asdf-powershell-core](https://github.com/daveneeley/asdf-powershell-core)                             |
| pre-commit                    | [jonathanmorley/asdf-pre-commit](https://github.com/jonathanmorley/asdf-pre-commit)                               |
| process-compose               | [martino/asdf-process-compose](https://github.com/martino/asdf-process-compose)                                   |
| promtool                      | [asdf-community/asdf-promtool](https://github.com/asdf-community/asdf-promtool)                                   |
| protoc                        | [paxosglobal/asdf-protoc](https://github.com/paxosglobal/asdf-protoc)                                             |
| protoc-gen-connect-go         | [dylanrayboss/asdf-protoc-gen-connect-go](https://github.com/dylanrayboss/asdf-protoc-gen-connect-go)             |
| protoc-gen-grpc-web           | [pbr0ck3r/asdf-protoc-gen-grpc-web](https://github.com/pbr0ck3r/asdf-protoc-gen-grpc-web)                         |
| protoc-gen-go-grpc            | [pbr0ck3r/asdf-protoc-gen-go-grpc](https://github.com/pbr0ck3r/asdf-protoc-gen-go-grpc)                           |
| protoc-gen-go                 | [pbr0ck3r/asdf-protoc-gen-go](https://github.com/pbr0ck3r/asdf-protoc-gen-go)                                     |
| protoc-gen-js                 | [pbr0ck3r/asdf-protoc-gen-js](https://github.com/pbr0ck3r/asdf-protoc-gen-js)                                     |
| protolint                     | [spencergilbert/asdf-protolint](https://github.com/spencergilbert/asdf-protolint)                                 |
| Proton GE                     | [augustobmoura/asdf-protonge](https://github.com/augustobmoura/asdf-protonge)                                     |
| psc-package                   | [nsaunders/asdf-psc-package](https://github.com/nsaunders/asdf-psc-package)                                       |
| Pulumi                        | [canha/asdf-pulumi](https://github.com/canha/asdf-pulumi)                                                         |
| purerl                        | [GoNZooo/asdf-purerl](https://github.com/GoNZooo/asdf-purerl)                                                     |
| PureScript                    | [jrrom/asdf-purescript](https://github.com/jrrom/asdf-purescript)                                                 |
| Purty                         | [nsaunders/asdf-purty](https://github.com/nsaunders/asdf-purty)                                                   |
| Python                        | [danhper/asdf-python](https://github.com/danhper/asdf-python)                                                     |
| q                             | [eheinle-mak/asdf-plugin-qdns](https://github.com/eheinle-mak/asdf-plugin-qdns)                                   |
| qsv                           | [vjda/asdf-qsv](https://github.com/vjda/asdf-qsv)                                                                 |
| Quarkus CLI                   | [asdf-community/asdf-quarkus](https://github.com/asdf-community/asdf-quarkus)                                     |
| R                             | [asdf-community/asdf-r](https://github.com/asdf-community/asdf-r)                                                 |
| RabbitMQ                      | [w-sanches/asdf-rabbitmq](https://github.com/w-sanches/asdf-rabbitmq)                                             |
| Racket                        | [asdf-community/asdf-racket](https://github.com/asdf-community/asdf-racket)                                       |
| Raku                          | [m-dango/asdf-raku](https://github.com/m-dango/asdf-raku)                                                         |
| Rancher                       | [abinet/asdf-rancher](https://github.com/abinet/asdf-rancher)                                                     |
| Rbac-lookup                   | [looztra/asdf-rbac-lookup](https://github.com/looztra/asdf-rbac-lookup)                                           |
| Rclone                        | [johnlayton/asdf-rclone](https://github.com/johnlayton/asdf-rclone)                                               |
| Rebar                         | [Stratus3D/asdf-rebar](https://github.com/Stratus3D/asdf-rebar)                                                   |
| Reckoner                      | [FairwindsOps/asdf-reckoner](https://github.com/FairwindsOps/asdf-reckoner)                                       |
| Redis                         | [smashedtoatoms/asdf-redis](https://github.com/smashedtoatoms/asdf-redis)                                         |
| Redis-cli                     | [NeoHsu/asdf-redis-cli](https://github.com/NeoHsu/asdf-redis-cli)                                                 |
| redo                          | [chessmango/asdf-redo](https://github.com/chessmango/asdf-redo)                                                   |
| redskyctl                     | [sudermanjr/asdf-redskyctl](https://github.com/sudermanjr/asdf-redskyctl)                                         |
| Reg                           | [looztra/asdf-reg](https://github.com/looztra/asdf-reg)                                                           |
| regal                         | [asdf-community/asdf-regal](https://github.com/asdf-community/asdf-regal)                                         |
| regctl                        | [ORCID/asdf-regctl](https://github.com/ORCID/asdf-regctl)                                                         |
| regsync                       | [rsrchboy/asdf-regsync](https://github.com/rsrchboy/asdf-regsync)                                                 |
| restic                        | [xataz/asdf-restic](https://github.com/xataz/asdf-restic)                                                         |
| resticprofile                 | [olofvndrhr/asdf-resticprofile](https://github.com/olofvndrhr/asdf-resticprofile)                                 |
| restish                       | [polds/asdf-restish](https://github.com/polds/asdf-restish)                                                       |
| revive                        | [bjw-s/asdf-revive](https://github.com/bjw-s/asdf-revive)                                                         |
| richgo                        | [paxosglobal/asdf-richgo](https://github.com/paxosglobal/asdf-richgo)                                             |
| Riff                          | [abinet/asdf-riff](https://github.com/abinet/asdf-riff)                                                           |
| ripgrep                       | [wt0f/asdf-ripgrep](https://gitlab.com/wt0f/asdf-ripgrep)                                                         |
| RKE                           | [particledecay/asdf-rke](https://github.com/particledecay/asdf-rke)                                               |
| rome                          | [kichiemon/asdf-rome](https://github.com/kichiemon/asdf-rome)                                                     |
| Redpanda RPK                  | [jleight/asdf-rpk](https://github.com/jleight/asdf-rpk)                                                           |
| rstash                        | [carlduevel/asdf-rstash](https://github.com/carlduevel/asdf-rstash)                                               |
| rlwrap                        | [asdf-community/asdf-rlwrap](https://github.com/asdf-community/asdf-rlwrap)                                       |
| Ruby                          | [asdf-vm/asdf-ruby](https://github.com/asdf-vm/asdf-ruby)                                                         |
| ruff                          | [simhem/asdf-ruff](https://github.com/simhem/asdf-ruff)                                                           |
| Rust                          | [code-lever/asdf-rust](https://github.com/code-lever/asdf-rust)                                                   |
| rust-analyzer                 | [Xyven1/asdf-rust-analyzer](https://github.com/Xyven1/asdf-rust-analyzer)                                         |
| rustic                        | [jahands/asdf-rustic](https://github.com/jahands/asdf-rustic)                                                     |
| rye                           | [Azuki-bar/asdf-rye](https://github.com/Azuki-bar/asdf-rye)                                                       |
| saml2aws                      | [elementalvoid/asdf-saml2aws](https://github.com/elementalvoid/asdf-saml2aws)                                     |
| SBT                           | [bram2000/asdf-sbt](https://github.com/bram2000/asdf-sbt)                                                         |
| scaffold                      | [particledecay/asdf-scaffold](https://github.com/particledecay/asdf-scaffold)                                     |
| Scala                         | [asdf-community/asdf-scala](https://github.com/asdf-community/asdf-scala)                                         |
| Scala CLI                     | [asdf-community/asdf-scala-cli](https://github.com/asdf-community/asdf-scala-cli)                                 |
| scaleway-cli                  | [albarralnunez/asdf-plugin-scaleway-cli](https://github.com/albarralnunez/asdf-plugin-scaleway-cli)               |
| scalingo-cli                  | [brandon-welsch/asdf-scalingo-cli](https://github.com/brandon-welsch/asdf-scalingo-cli)                           |
| Scarb                         | [software-mansion/asdf-scarb](https://github.com/software-mansion/asdf-scarb)                                     |
| sccache                       | [emersonmx/asdf-sccache](https://github.com/emersonmx/asdf-sccache)                                               |
| Scenery                       | [skyzyx/asdf-scenery](https://github.com/skyzyx/asdf-scenery)                                                     |
| schemacrawler                 | [davidecavestro/asdf-schemacrawler](https://github.com/davidecavestro/asdf-schemacrawler)                         |
| scie-pants                    | [robzr/asdf-scie-pants](https://github.com/robzr/asdf-scie-pants)                                                 |
| Seed7                         | [susurri/asdf-seed7](https://github.com/susurri/asdf-seed7)                                                       |
| Semgrep                       | [brentjanderson/asdf-semgrep](https://github.com/brentjanderson/asdf-semgrep)                                     |
| semtag                        | [junminahn/asdf-semtag](https://github.com/junminahn/asdf-semtag)                                                 |
| semver                        | [mathew-fleisch/asdf-semver](https://github.com/mathew-fleisch/asdf-semver)                                       |
| Sentinel                      | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| sentry-cli                    | [MacPaw/asdf-sentry-cli](https://github.com/MacPaw/asdf-sentry-cli)                                               |
| Serf                          | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| serverless                    | [pdemagny/asdf-serverless](https://github.com/pdemagny/asdf-serverless)                                           |
| shell2http                    | [ORCID/asdf-shell2http](https://github.com/ORCID/asdf-shell2http)                                                 |
| Shellcheck                    | [luizm/asdf-shellcheck](https://github.com/luizm/asdf-shellcheck)                                                 |
| Shellspec                     | [poikilotherm/asdf-shellspec](https://github.com/poikilotherm/asdf-shellspec)                                     |
| Shfmt                         | [luizm/asdf-shfmt](https://github.com/luizm/asdf-shfmt)                                                           |
| Shorebird                     | [valian-ca/asdf-shorebird](https://github.com/valian-ca/asdf-shorebird)                                           |
| signal-cli                    | [ehsash/asdf-signal-cli](https://github.com/ehsash/asdf-signal-cli)                                               |
| Sinker                        | [elementalvoid/asdf-sinker](https://github.com/elementalvoid/asdf-sinker)                                         |
| Skaffold                      | [nklmilojevic/asdf-skaffold](https://github.com/nklmilojevic/asdf-skaffold)                                       |
| skate                         | [chessmango/asdf-skate](https://github.com/chessmango/asdf-skate)                                                 |
| Sloth                         | [slok/asdf-sloth](https://github.com/slok/asdf-sloth)                                                             |
| smithy                        | [aws/asdf-smithy](https://github.com/aws/asdf-smithy)                                                             |
| SML/NJ                        | [samontea/asdf-smlnj](https://github.com/samontea/asdf-smlnj)                                                     |
| Snyk                          | [nirfuchs/asdf-snyk](https://github.com/nirfuchs/asdf-snyk)                                                       |
| soft-serve                    | [chessmango/asdf-soft-serve](https://github.com/chessmango/asdf-soft-serve)                                       |
| Solidity                      | [diegodorado/asdf-solidity](https://github.com/diegodorado/asdf-solidity)                                         |
| Sonobuoy                      | [Nick-Triller/asdf-sonobuoy](https://github.com/Nick-Triller/asdf-sonobuoy)                                       |
| Sops                          | [feniix/asdf-sops](https://github.com/feniix/asdf-sops)                                                           |
| sopstool                      | [elementalvoid/asdf-sopstool](https://github.com/elementalvoid/asdf-sopstool)                                     |
| soracom-cli                   | [gr1m0h/asdf-soracom](https://github.com/gr1m0h/asdf-soracom)                                                     |
| Sourcery                      | [younke/asdf-sourcery](https://github.com/younke/asdf-sourcery)                                                   |
| spacectl                      | [bodgit/asdf-spacectl](https://github.com/bodgit/asdf-spacectl)                                                   |
| Spago                         | [jrrom/asdf-spago](https://github.com/jrrom/asdf-spago)                                                           |
| Spark                         | [jeffryang24/asdf-spark](https://github.com/jeffryang24/asdf-spark)                                               |
| Spectral                      | [vbyrd/asdf-spectral](https://github.com/vbyrd/asdf-spectral)                                                     |
| Spin                          | [pavloos/asdf-spin](https://github.com/pavloos/asdf-spin)                                                         |
| spotbugs                      | [jiahuili430/asdf-spotbugs](https://github.com/jiahuili430/asdf-spotbugs)                                         |
| Spring Boot CLI               | [joschi/asdf-spring-boot](https://github.com/joschi/asdf-spring-boot)                                             |
| Spruce                        | [woneill/asdf-spruce](https://github.com/woneill/asdf-spruce)                                                     |
| sqlc                          | [dylanrayboss/asdf-sqlc](https://github.com/dylanrayboss/asdf-sqlc)                                               |
| sqldef                        | [cometkim/asdf-sqldef](https://github.com/cometkim/asdf-sqldef)                                                   |
| SQLite                        | [cLupus/asdf-sqlite](https://github.com/cLupus/asdf-sqlite)                                                       |
| sshuttle                      | [xanmanning/asdf-sshuttle](https://github.com/xanmanning/asdf-sshuttle)                                           |
| sst                           | [nurulhudaapon/asdf-sst](https://github.com/nurulhudaapon/asdf-sst)                                               |
| Stack                         | [sestrella/asdf-ghcup](https://github.com/sestrella/asdf-ghcup)                                                   |
| starboard                     | [zufardhiyaulhaq/asdf-starboard](https://github.com/zufardhiyaulhaq/asdf-starboard)                               |
| Starkli                       | [ptisserand/asdf-starkli](https://github.com/ptisserand/asdf-starkli)                                             |
| Starknet Devnet               | [ptisserand/asdf-starknet-devnet](https://github.com/ptisserand/asdf-starknet-devnet)                             |
| Starknet Foundry              | [foundry-rs/asdf-starknet-foundry](https://github.com/foundry-rs/asdf-starknet-foundry)                           |
| starport                      | [nikever/asdf-starport](https://github.com/nikever/asdf-starport)                                                 |
| starship                      | [gr1m0h/asdf-starship](https://github.com/gr1m0h/asdf-starship)                                                   |
| Staticcheck                   | [pbr0ck3r/asdf-staticcheck](https://github.com/pbr0ck3r/asdf-staticcheck)                                         |
| steampipe                     | [carnei-ro/asdf-steampipe](https://github.com/carnei-ro/asdf-steampipe)                                           |
| Steel Bank Common Lisp (sbcl) | [smashedtoatoms/asdf-sbcl](https://github.com/smashedtoatoms/asdf-sbcl)                                           |
| step                          | [log2/asdf-step](https://github.com/log2/asdf-step)                                                               |
| Stern                         | [looztra/asdf-stern](https://github.com/looztra/asdf-stern)                                                       |
| stratus-red-team              | [asdf-community/asdf-stratus-red-team](https://github.com/asdf-community/asdf-stratus-red-team)                   |
| stripe-cli                    | [offbyone/asdf-stripe](https://github.com/offbyone/asdf-stripe)                                                   |
| stylua                        | [jc00ke/asdf-stylua](https://github.com/jc00ke/asdf-stylua)                                                       |
| sui                           | [placeholder-soft/asdf-sui](https://github.com/placeholder-soft/asdf-sui)                                         |
| supabase-cli                  | [gavinying/asdf-supabase-cli](https://github.com/gavinying/asdf-supabase-cli)                                     |
| sver                          | [robzr/asdf-sver](https://github.com/robzr/asdf-sver)                                                             |
| svu                           | [asdf-community/asdf-svu](https://github.com/asdf-community/asdf-svu)                                             |
| swag                          | [behoof4mind/asdf-swag](https://github.com/behoof4mind/asdf-swag)                                                 |
| Swift                         | [fcrespo82/asdf-swift](https://github.com/fcrespo82/asdf-swift)                                                   |
| SwiftFormat                   | [younke/asdf-swiftformat](https://github.com/younke/asdf-swiftformat)                                             |
| SwiftGen                      | [younke/asdf-swiftgen](https://github.com/younke/asdf-swiftgen)                                                   |
| Swiftlint                     | [klundberg/asdf-swiftlint](https://github.com/klundberg/asdf-swiftlint)                                           |
| SWIProlog                     | [mracos/asdf-swiprolog](https://github.com/mracos/asdf-swiprolog)                                                 |
| syft                          | [davidgp1701/asdf-syft](https://github.com/davidgp1701/asdf-syft)                                                 |
| sync                          | [robzr/asdf-sync](https://github.com/robzr/asdf-sync)                                                             |
| syncher                       | [nwillc/syncher](https://github.com/nwillc/syncher)                                                               |
| talhelper                     | [bjw-s/asdf-talhelper](https://github.com/bjw-s/asdf-talhelper)                                                   |
| Talos                         | [particledecay/asdf-talos](https://github.com/particledecay/asdf-talos)                                           |
| talosctl                      | [bjw-s/asdf-talosctl](https://github.com/bjw-s/asdf-talosctl)                                                     |
| Tanka                         | [trotttrotttrott/asdf-tanka](https://github.com/trotttrotttrott/asdf-tanka)                                       |
| Tanzu CLI (tanzu)             | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| Task                          | [particledecay/asdf-task](https://github.com/particledecay/asdf-task)                                             |
| tctl                          | [eko/asdf-tctl](https://github.com/eko/asdf-tctl)                                                                 |
| Tekton-cli                    | [johnhamelink/asdf-tekton-cli](https://github.com/johnhamelink/asdf-tekton-cli)                                   |
| Tekton pipeline-as-code CLI   | [ifireball/asdf-tekton-pac-cli](https://github.com/ifireball/asdf-tekton-pac-cli)                                 |
| Teleport Enterprise           | [highb/asdf-teleport-ent](https://github.com/highb/asdf-teleport-ent)                                             |
| Teleport Community            | [MaloPolese/asdf-teleport-community](https://github.com/MaloPolese/asdf-teleport-community)                       |
| telepresence                  | [pirackr/asdf-telepresence](https://github.com/pirackr/asdf-telepresence)                                         |
| teller                        | [pdemagny/asdf-teller](https://github.com/pdemagny/asdf-teller)                                                   |
| temporal                      | [asdf-community/asdf-temporal](https://github.com/asdf-community/asdf-temporal)                                   |
| temporalite                   | [eko/asdf-temporalite](https://github.com/eko/asdf-temporalite)                                                   |
| terradozer                    | [chessmango/asdf-terradozer](https://github.com/chessmango/asdf-terradozer)                                       |
| Terraform                     | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| Terraform-docs                | [looztra/asdf-terraform-docs](https://github.com/looztra/asdf-terraform-docs)                                     |
| terraform-ls                  | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| terraform-lsp                 | [bartlomiejdanek/asdf-terraform-lsp](https://github.com/bartlomiejdanek/asdf-terraform-lsp)                       |
| Terraform-validator           | [looztra/asdf-terraform-validator](https://github.com/looztra/asdf-terraform-validator)                           |
| Terraformer                   | [gr1m0h/asdf-terraformer](https://github.com/gr1m0h/asdf-terraformer)                                             |
| Terragrunt                    | [gruntwork-io/asdf-terragrunt](https://github.com/gruntwork-io/asdf-terragrunt)                                   |
| Terramate                     | [martinlindner/asdf-terramate](https://github.com/martinlindner/asdf-terramate)                                   |
| Terrascan                     | [hpdobrica/asdf-terrascan](https://github.com/hpdobrica/asdf-terrascan)                                           |
| tf (hashi terraform wrapper)  | [dex4er/asdf-tf](https://github.com/dex4er/asdf-tf)                                                               |
| tfcmt                         | [nasa9084/asdf-tfcmt](https://github.com/nasa9084/asdf-tfcmt)                                                     |
| tfctl                         | [deas/asdf-tfctl](https://github.com/deas/asdf-tfctl)                                                             |
| tfc-agent                     | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| tfenv                         | [carlduevel/asdf-tfenv](https://github.com/carlduevel/asdf-tfenv)                                                 |
| TFLint                        | [skyzyx/asdf-tflint](https://github.com/skyzyx/asdf-tflint)                                                       |
| tfmigrate                     | [dex4er/asdf-tfmigrate](https://github.com/dex4er/asdf-tfmigrate)                                                 |
| tfnotify                      | [jnavarrof/asdf-tfnotify](https://github.com/jnavarrof/asdf-tfnotify)                                             |
| TFSec                         | [woneill/asdf-tfsec](https://github.com/woneill/asdf-tfsec)                                                       |
| tfstate-lookup                | [carnei-ro/asdf-tfstate-lookup](https://github.com/carnei-ro/asdf-tfstate-lookup)                                 |
| tfswitch                      | [iul1an/asdf-tfswitch](https://github.com/iul1an/asdf-tfswitch)                                                   |
| tfupdate                      | [yuokada/asdf-tfupdate](https://github.com/yuokada/asdf-tfupdate)                                                 |
| tf-summarize                  | [adamcrews/asdf-tf-summarize](https://github.com/adamcrews/asdf-tf-summarize)                                     |
| Thrift                        | [alisaifee/asdf-thrift](https://github.com/alisaifee/asdf-thrift)                                                 |
| Tilt                          | [eaceaser/asdf-tilt](https://github.com/eaceaser/asdf-tilt)                                                       |
| Timoni                        | [Smana/asdf-timoni](https://github.com/Smana/asdf-timoni)                                                         |
| Tinytex                       | [Fbrisset/asdf-tinytex](https://github.com/Fbrisset/asdf-tinytex)                                                 |
| Titan                         | [gabitchov/asdf-titan](https://github.com/gabitchov/asdf-titan)                                                   |
| tlsg-cli                      | [0ghny/asdf-tlsgcli](https://github.com/0ghny/asdf-tlsgcli)                                                       |
| Tmux                          | [pauloedurezende/asdf-tmux](https://github.com/pauloedurezende/asdf-tmux)                                         |
| Tokei                         | [gasuketsu/asdf-tokei](https://github.com/gasuketsu/asdf-tokei)                                                   |
| tomcat                        | [asdf-community/asdf-tomcat](https://github.com/asdf-community/asdf-tomcat)                                       |
| tonnage                       | [elementalvoid/asdf-tonnage](https://github.com/elementalvoid/asdf-tonnage)                                       |
| tool-versions-to-env          | [smartcontractkit/tool-versions-to-env-action](https://github.com/smartcontractkit/tool-versions-to-env-action)   |
| Traefik                       | [Dabolus/asdf-traefik](https://github.com/Dabolus/asdf-traefik)                                                   |
| Trdsql                        | [johnlayton/asdf-trdsql](https://github.com/johnlayton/asdf-trdsql)                                               |
| tree-sitter                   | [ivanvc/asdf-tree-sitter](https://github.com/ivanvc/asdf-tree-sitter)                                             |
| tridentctl                    | [asdf-community/asdf-tridentctl](https://github.com/asdf-community/asdf-tridentctl)                               |
| Trivy                         | [zufardhiyaulhaq/asdf-trivy](https://github.com/zufardhiyaulhaq/asdf-trivy)                                       |
| tsuru                         | [virtualstaticvoid/asdf-tsuru](https://github.com/virtualstaticvoid/asdf-tsuru)                                   |
| tttyd                         | [ivanvc/asdf-ttyd](https://github.com/ivanvc/asdf-ttyd)                                                           |
| tuist                         | [asdf-community/asdf-tuist](https://github.com/asdf-community/asdf-tuist)                                         |
| tx                            | [ORCID/asdf-transifex](https://github.com/ORCID/asdf-transifex)                                                   |
| typos                         | [aschiavon91/asdf-typos](https://github.com/aschiavon91/asdf-typos)                                               |
| typst                         | [stephane-klein/asdf-typst](https://github.com/stephane-klein/asdf-typst)                                         |
| uaa-cli                       | [vmware-tanzu/tanzu-plug-in-for-asdf](https://github.com/vmware-tanzu/tanzu-plug-in-for-asdf)                     |
| Unison                        | [susurri/asdf-unison](https://github.com/susurri/asdf-unison)                                                     |
| updatecli                     | [updatecli/asdf-updatecli](https://github.com/updatecli/asdf-updatecli)                                           |
| upt                           | [ORCID/asdf-upt](https://github.com/ORCID/asdf-upt)                                                               |
| upx                           | [jimmidyson/asdf-upx](https://github.com/jimmidyson/asdf-upx)                                                     |
| usql                          | [itspngu/asdf-usql](https://github.com/itspngu/asdf-usql)                                                         |
| uv                            | [asdf-community/asdf-uv](https://github.com/asdf-community/asdf-uv)                                               |
| V                             | [jthegedus/asdf-v](https://github.com/jthegedus/asdf-v)                                                           |
| vale                          | [pdemagny/asdf-vale](https://github.com/pdemagny/asdf-vale)                                                       |
| vals                          | [dex4er/asdf-vals](https://github.com/dex4er/asdf-vals)                                                           |
| Vault                         | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| Velero                        | [looztra/asdf-velero](https://github.com/looztra/asdf-velero)                                                     |
| vendir                        | [vmware-tanzu/asdf-carvel](https://github.com/vmware-tanzu/asdf-carvel)                                           |
| Venom                         | [aabouzaid/asdf-venom](https://github.com/aabouzaid/asdf-venom)                                                   |
| versio                        | [pdemagny/asdf-versio](https://github.com/pdemagny/asdf-versio)                                                   |
| vcluster                      | [wt0f/asdf-vcluster](https://gitlab.com/wt0f/asdf-vcluster)                                                       |
| vela                          | [pdemagny/asdf-vela](https://github.com/pdemagny/asdf-vela)                                                       |
| velad                         | [pdemagny/asdf-velad](https://github.com/pdemagny/asdf-velad)                                                     |
| vhs                           | [chessmango/asdf-vhs](https://github.com/chessmango/asdf-vhs)                                                     |
| Viddy                         | [ryodocx/asdf-viddy](https://github.com/ryodocx/asdf-viddy)                                                       |
| Vim                           | [tsuyoshicho/asdf-vim](https://github.com/tsuyoshicho/asdf-vim)                                                   |
| vlt                           | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| vultr-cli                     | [ikuradon/asdf-vultr-cli](https://github.com/ikuradon/asdf-vultr-cli)                                             |
| watchexec                     | [nyrst/asdf-watchexec](https://github.com/nyrst/asdf-watchexec)                                                   |
| WASI SDK                      | [coolreader18/asdf-wasi-sdk](https://github.com/coolreader18/asdf-wasi-sdk)                                       |
| WASM-4                        | [jtakakura/asdf-wasm4](https://github.com/jtakakura/asdf-wasm4)                                                   |
| wasm3                         | [tachyonicbytes/asdf-wasm3](https://github.com/tachyonicbytes/asdf-wasm3)                                         |
| wasmer                        | [tachyonicbytes/asdf-wasmer](https://github.com/tachyonicbytes/asdf-wasmer)                                       |
| wasmtime                      | [tachyonicbytes/asdf-wasmtime](https://github.com/tachyonicbytes/asdf-wasmtime)                                   |
| Waypoint                      | [asdf-community/asdf-hashicorp](https://github.com/asdf-community/asdf-hashicorp)                                 |
| weave-gitops                  | [deas/asdf-weave-gitops](https://github.com/deas/asdf-weave-gitops)                                               |
| Websocat                      | [bdellegrazie/asdf-websocat](https://github.com/bdellegrazie/asdf-websocat)                                       |
| woodpecker-cli                | [ivanvc/asdf-woodpecker](https://github.com/ivanvc/asdf-woodpecker)                                               |
| Wren CLI                      | [jtakakura/asdf-wren-cli](https://github.com/jtakakura/asdf-wren-cli)                                             |
| wrk                           | [ivanvc/asdf-wrk](https://github.com/ivanvc/asdf-wrk)                                                             |
| Wtfutil                       | [NeoHsu/asdf-wtfutil](https://github.com/NeoHsu/asdf-wtfutil)                                                     |
| XCTestHTMLReport              | [younke/asdf-xchtmlreport](https://github.com/younke/asdf-xchtmlreport)                                           |
| XcodeGen                      | [younke/asdf-xcodegen](https://github.com/younke/asdf-xcodegen)                                                   |
| xc                            | [airtonix/asdf-xc](https://github.com/airtonix/asdf-xc)                                                           |
| xcbeautify                    | [MacPaw/asdf-xcbeautify](https://github.com/MacPaw/asdf-xcbeautify)                                               |
| xcodes                        | [younke/asdf-xcodes](https://github.com/younke/asdf-xcodes)                                                       |
| xcresultparser                | [MacPaw/asdf-xcresultparser](https://github.com/MacPaw/asdf-xcresultparser)                                       |
| xh                            | [NeoHsu/asdf-xh](https://github.com/NeoHsu/asdf-xh)                                                               |
| yadm                          | [particledecay/asdf-yadm](https://github.com/particledecay/asdf-yadm)                                             |
| yamlfmt                       | [mise-plugins/asdf-yamlfmt](https://github.com/mise-plugins/asdf-yamlfmt)                                         |
| yamllint                      | [ericcornelissen/asdf-yamllint](https://github.com/ericcornelissen/asdf-yamllint)                                 |
| yamlscript                    | [FeryET/asdf-yamlscript](https://github.com/FeryET/asdf-yamlscript)                                               |
| Yarn                          | [twuni/asdf-yarn](https://github.com/twuni/asdf-yarn)                                                             |
| Yasm                          | [kkHAIKE/asdf-yasm](https://github.com/kkHAIKE/asdf-yasm)                                                         |
| yay                           | [aaaaninja/asdf-yay](https://github.com/aaaaninja/asdf-yay)                                                       |
| Yor                           | [ordinaryexperts/asdf-yor](https://github.com/ordinaryexperts/asdf-yor)                                           |
| youtube-dl                    | [iul1an/asdf-youtube-dl](https://github.com/iul1an/asdf-youtube-dl)                                               |
| yj                            | [ryodocx/asdf-yj](https://github.com/ryodocx/asdf-yj)                                                             |
| yq                            | [sudermanjr/asdf-yq](https://github.com/sudermanjr/asdf-yq)                                                       |
| yt-dlp                        | [duhow/asdf-yt-dlp](https://github.com/duhow/asdf-yt-dlp)                                                         |
| ytt                           | [vmware-tanzu/asdf-carvel](https://github.com/vmware-tanzu/asdf-carvel)                                           |
| zbctl                         | [camunda-community-hub/asdf-zbctl](https://github.com/camunda-community-hub/asdf-zbctl)                           |
| zellij                        | [chessmango/asdf-zellij](https://github.com/chessmango/asdf-zellij)                                               |
| Zephyr                        | [nsaunders/asdf-zephyr](https://github.com/nsaunders/asdf-zephyr)                                                 |
| Zig                           | [cheetah/asdf-zig](https://github.com/cheetah/asdf-zig)                                                           |
| zigmod                        | [mise-plugins/asdf-zigmod](https://github.com/mise-plugins/asdf-zigmod)                                           |
| zls                           | [miome/asdf-zls](https://github.com/m1ome/asdf-zls)                                                               |
| Zola                          | [salasrod/asdf-zola](https://github.com/salasrod/asdf-zola)                                                       |
| zoxide                        | [nyrst/asdf-zoxide](https://github.com/nyrst/asdf-zoxide)                                                         |
| zprint                        | [carlduevel/asdf-zprint](https://github.com/carlduevel/asdf-zprint)                                               |
