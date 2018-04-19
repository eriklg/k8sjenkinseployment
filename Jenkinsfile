node {

  def imageTag = "docker.io/elustgarten/djangosample:${env.BUILD_NUMBER}"

  checkout scm
  
  stage 'Build image'
  sh("sudo docker build -t ${imageTag} -f src/Dockerfile")

  stage 'Docker login'
  sh("sudo docker login -u elustgarten@apprenda.com -p @ppr3nd@")

  stage 'Push image to registry'
  sh("sudo docker push ${imageTag}")
}