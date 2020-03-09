def label = "slave-${UUID.randomUUID().toString()}"
pipeline {
    agent any
	parameters{string defautValue:'',description:'请输入代码路径,GIT只需要输入SHA值,SVN需要输入完整的路径和版本号',name: 'CODE_PATH',trim:true}
    stages{
		stage('0.定义slave名称'){
			steps{
			  script {
				echo "${label}"
			  }
			}
		
		}
	}
	stages{
        stage('Pull Git Demo') {
            steps{
                //拉取代码，这里也是可以使用凭据的，为了方便没贴出来
                git 'https://github.com/hudepin/springboot-demo'
            }
        }
   }
}