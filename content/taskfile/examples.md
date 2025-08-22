---
weight: 60
---
{{% section %}}

### How to use

Task will look for the following file names, in order of priority:
{{< lines >}}
- Taskfile.yml
- Taskfile.yaml
- Taskfile.dist.yml
- Taskfile.dist.yaml
{{< /lines >}}

------

### Basic example

{{< code lang="yaml" line-numbers="true" >}}
version: '3'

tasks:
  build:
    cmds:
      - go build -v -i main.go

  assets:
    cmds:
      - esbuild --bundle --minify css/index.css > public/bundle.css
{{< /code >}}

------
### Running from subdirectories

{{< code lang="yaml" line-numbers="true" >}}
version: '3'

tasks:
  up:
    dir: '{{.USER_WORKING_DIR}}'
    preconditions:
      - test -f docker-compose.yml
    cmds:
      - docker-compose up -d
{{< /code >}}

------
### Including other `Taskfiles`

{{< code lang="yaml" line-numbers="true" >}}
version: '3'

includes:
  docs: ./documentation # will look for ./documentation/Taskfile.yml
  docker: ./DockerTasks.yml
{{< /code >}}

------
### Dependencies and preconditions

{{< code lang="yaml" line-numbers="true" focus="|4|9-11|13|18-20|22|27-29|30-32" >}}
version: '3'

tasks:
  build:
    desc: Build the project
    cmds:
      - npm install
      - npm run build
    preconditions:
      - sh: command -v npm
        msg: "npm not found, please install it"

  test:
    desc: Run tests
    cmds:
      - task build
      - npm test
    preconditions:
      - sh: command -v npm
        msg: "npm not found, please install it"

  deploy:
    desc: Deploy the project
    cmds:
      - task test
      - npm run deploy
    deps:
      - build
      - test
    preconditions:
      - sh: command -v npm
        msg: "npm not found, please install it"
{{< /code >}}

{{% /section %}}
