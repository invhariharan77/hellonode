node {
    git 'https://github.com/fabric8-quickstarts/node-example.git'
    if (!fileExists ('Dockerfile')) {
      writeFile file: 'Dockerfile', text: 'FROM node:5.3-onbuild'
    }
    kubernetes.image().withName("example").build().fromPath(".")
}
