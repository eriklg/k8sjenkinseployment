node {

  def imageTag = "docker.io/elustgarten/djangosample:${env.BUILD_NUMBER}"

  checkout scm

  stage 'Print hello'
  sh("echo hello")
  
  stage 'Build image'
  sh("docker build -t ${imageTag} -f src/Dockerfile")

  stage 'Docker login'
  sh("docker login -u elustgarten@apprenda.com -p @ppr3nd@")

  stage 'Push image to registry'
  sh("docker push ${imageTag}")
}