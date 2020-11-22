# Monorepos

## Concept

A `Monorepository` is an architectural concept,
which basically contains all the meaning in its title.
Instead of managing multiple repositories,
you keep all your isolated code parts inside one repository.
Keep in mind the word isolated - it means that monorepo has nothing in common with monolithic apps.
You can keep many kinds of logical apps inside one repo;
for example, a website and its iOS app.

## Advantages

- One place to store all configs and tests.
  you can configure your CI/CD and bundler once and then just re-use configs to build all packages before publishing them to remote.

- Easily refactor global features with atomic commits.
  Instead of doing a pull request for each repo,
  figuring out in which order to build your change,
  you just need to make an atomic pull request which will contain all commits related to the feature that you are working against.

- Simplified package publishing.
  If you plan to implement a new feature inside a package that is dependent on another package with shared code,
  you can do it with a single command.

- Easier dependency management.
  Only one package.json.

- Re-use code with shared packages while still keeping them isolated.
  Monorepo allows you to reuse your packages from other packages while keeping them isolated from one another.
  You can use a reference to the remote package and consume them via a single entry point.
  To use the local version, you are able to use local symlinks.
  This feature can be implemented via bash scripts or by introducing some additional tools like Lerna or Yarn.
