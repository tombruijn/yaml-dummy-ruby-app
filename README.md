# Psych error app

## Requirements

- Docker

## Usage

```
./script
```

### Steps the script takes

- Calling `./script` will start a Docker container with Ruby 3.1.
- In the container the `./inner_script` will be run.
- Required build dependencies are installed.
- Psych gem version 5 is installed using `gem install psych --version 5.0.2`.
- `bundle install` is run, which installs this [example gem](https://github.com/tombruijn/yaml-dummy-gem) that parses YAML during extension installation.
- An error is raised upon the parsing of a YAML string.
- `bundle install` exits with a failure.
