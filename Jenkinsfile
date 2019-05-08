// 测试环境Jenkinsfile
def envKey = env.JOB_NAME.substring(0,1)
def domainName, namespace, portPrefix, springConfigLabel, serviceAddr
switch (envKey) {
    case "d":
       domainName = "d.haimaxy.com"
       namespace = "oliver-dev"
       break
    default:
        println("No matching case found!!")

}
def registryUrl = "harbor.haimaxy.com"
def registryCredential = "harbor"

def projectName = env.JOB_NAME.substring(2, env.JOB_NAME.length())
def jobName = env.JOB_NAME.trim()
def gitBranch = params.BRANCH.trim()
def gitUrl = "https://github.com/luochengyuan123/${env.JOB_NAME.substring(2, env.JOB_NAME.length())}.git"
def gitCredential = "gitlabjenkins"
def imageTag = sh(script: "git rev-parse --short HEAD", returnStdout: true).trim()
def imageEndpoint = "payeco/${projectName}"
def image = "${registryUrl}/${imageEndpoint}"


node('jenkins-jnlp') {
    stage('单元测试') {
      echo "测试阶段"
    }
    stage('代码编译打包') {
      
        echo "代码编译打包阶段"
      
    }
    stage('构建 Docker 镜像') {
      
        echo "构建 Docker 镜像阶段"
      
    }
    stage('运行 Kubectl') {
      
        echo "查看 K8S 集群 Pod 列表"
        sh "kubectl get pods"
      
    }
}
