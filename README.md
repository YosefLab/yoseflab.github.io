# yoseflab.github.io

Based on [this](https://github.com/alshedivat/al-folio) Jekyll theme.

Commits to `source` branch get deployed automatically.

For local development, you need to install Ruby and Jekyll. You can easily
install these requirements in a conda environment:

```bash
$ conda create -n Ruby ruby rb-jekyll
$ source activate Ruby
```

To view changes:

```bash
$ bundle install
$ bundle exec jekyll serve
```

If you get the following error during installation:

```bash
	make: x86_64-apple-darwin13.4.0-clang: No such file or directory
````

you may need to first install clang:

```bash
$ conda install clangxx_osx-64
$ export CONDA_BUILD_SYSROOT=$(xcrun --show-sdk-path)
```

Update lab member info in `_data/members.yml`, publication info in `_data/publications.yml`.
