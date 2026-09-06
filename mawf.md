ci.yml:
```yaml
name: Node.js 24 Production CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build-and-test:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository code
      uses: actions/checkout@v4

    - name: Set up Node.js 24 (LTS)
      uses: actions/setup-node@v4
      with:
        node-version: '24'

    - name: Install dependencies
      run: npm ci

    - name: Run tests
      run: npm test
```
<Ending>
Now your workflow is created!
</Ending>
