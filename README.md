# chombo-action
Github Action to download and compile Chombo, for use as a dependency for compiling against.

# Example

```yaml
on: [push]

jobs:
  your_job:
    runs-on: ubuntu-latest
    name: Build with Chombo
    steps:
    - uses: actions/checkout@v2
    - uses: jrgparkinson/chombo-action@v1
      with:
        compile_opts: 'DIM=3'

    - name: Build your application
      run: |
        echo $CHOMBO_HOME
        make

```