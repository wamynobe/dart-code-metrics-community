# Dart Code Metrics (Community Edition)

This is a community-driven fork of the original Dart Code Metrics project, a toolkit that helps you identify and fix problems in your Dart and Flutter code. It includes over 70 built-in rules to validate your code against various expectations, and you can customize these rules to fit your specific needs.

*Note:* This readme reflects the community edition and might not have all the features available in the original project.

Installation
```bash
$ dart pub add --dev dart_code_metrics
```
or for a Flutter package
```base
$ flutter pub add --dev dart_code_metrics
```


## Basic Configuration
Add configuration to analysis_options.yaml and reload IDE to allow the analyzer to discover the plugin config.

You can find more information about the configuration options in the original documentation: https://dcm.dev/docs/individuals/configuration/.  We are working on replicating this information here.

### Basic config example
```yaml
analyzer:
  plugins:
    - dart_code_metrics

dart_code_metrics:
  rules:
    - avoid-dynamic
    - avoid-passing-async-when-sync-expected
    - avoid-redundant-async
    - avoid-unnecessary-type-assertions
    - avoid-unnecessary-type-casts
    - avoid-unrelated-type-assertions
    - avoid-unused-parameters
    - avoid-nested-conditional-expressions
    - newline-before-return
    - no-boolean-literal-compare
    - no-empty-block
    - prefer-trailing-comma
    - prefer-conditional-expressions
    - no-equal-then-else
    - prefer-moving-to-variable
    - prefer-match-file-name
```

### Basic config with metrics
```yaml
analyzer:
  plugins:
    - dart_code_metrics

dart_code_metrics:
  metrics:
    cyclomatic-complexity: 20
    number-of-parameters: 4
    maximum-nesting-level: 5
  metrics-exclude:
    - test/**
  rules:
    - avoid-dynamic
    - avoid-passing-async-when-sync-expected
    - avoid-redundant-async
    - avoid-unnecessary-type-assertions
    - avoid-unnecessary-type-casts
    - avoid-unrelated-type-assertions
    - avoid-unused-parameters
    - avoid-nested-conditional-expressions
    - newline-before-return
    - no-boolean-literal-compare
    - no-empty-block
    - prefer-trailing-comma
    - prefer-conditional-expressions
    - no-equal-then-else
    - prefer-moving-to-variable
    - prefer-match-file-name
```

## Usage
Analyzer plugin
DCM can be used as a plugin for the Dart analyzer package providing additional rules. All issues produced by rules or anti-patterns will be highlighted in IDE.

Rules that marked with  have auto-fixes available through the IDE context menu.

## CLI
The package can be used as CLI and supports multiple commands (see original documentation for details). Note that some functionalities might be missing in this community edition.

We are currently working on adding detailed instructions and examples for the CLI commands.

For additional help, you can refer to the original documentation (https://github.com/dart-code-checker/dart-code-metrics) or ask questions in our community forum (link coming soon!).

## Troubleshooting
If you encounter any issues, please create a new issue on the project's issue tracker: URL github issue dart code checker ON github.com.

We appreciate your help in improving this community edition!

Contributing
We welcome contributions from the community! You can submit bug reports, feature requests, or pull requests through the GitHub repository.

Please refer to the contributing guidelines: URL dart code metrics contributing guidelines ON GitHub github.com (work in progress) for more details.

## Community
Join our community forum (link coming soon!) to discuss the project, share your experiences, and get help from other users.

## License
[MIT](./LICENSE)
