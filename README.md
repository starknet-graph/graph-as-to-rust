# `graph-as-to-rust` Fork for StarkNet

This is a [`graph-as-to-rust`](https://github.com/streamingfast/graph-as-to-rust) fork for code generation for [StarkNet](https://starknet.io/) to be used in our [`graph-node` fork](https://github.com/starknet-graph/graph-node). It's created and maintained by the [zkLend](https://zklend.com/) team.

The original upstream repository is hard-coded to generate code for `near`. Instead of maintaining documentation on how to change the hard-coded values, we decided to fork it instead to provide an out of the box solution.

Powered by a [GitHub Actions workflow](https://github.com/starknet-graph/graph-as-to-rust/actions/workflows/sync.yml), this fork syncs the `master` branch with the upstream continuously:

- First, a commit is made on top of the upstream `master` branch to bring files from the [`home`](https://github.com/starknet-graph/graph-as-to-rust/tree/home) branch to `master`. This is necessary for making changes to CI workflows and the README file you're reading right now.

- Then, actual patch commits living on the fork `master` branch gets rebased. Before pushing, the branch is compiled to make sure it still builds, and the team gets notified if it doesn't.

Whenever a version is released on the upstream project, we will make the same release except with the patch applied.
