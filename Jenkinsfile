def myfn() {
	println "my first fuction cdoe"
}
def mysumfn(a,b) {
	sum =a+b
	println "My fun with pram sum of a + b is ${sum} " 
}
pipeline {
	agent {
        	label '!windows'
    	}
    	environment {
        	DISABLE_AUTH = 'true'
        	DB_ENGINE    = 'sqlite'
    	}
	parameters {
		choice choices: ['Dev', 'SIT', 'QA', 'PROD'], name: 'ENV'
		string defaultValue:'1.1.1', name: 'VERSION'
	}
	
	stages {
		stage("working with file operations") {
			steps {
				script {
					var1=10
					var2="value is 10"
					println "The value of var1 is ${var1}, value of var2 is ${var2}"
					println "Print-Database engine is ${env.DB_ENGINE}"
					println "Print DISABLE_AUTH is ${env.DISABLE_AUTH}"
					echo "Database engine is ${DB_ENGINE}"
					echo "DISABLE_AUTH is ${DISABLE_AUTH}"
					println "Env selected is ${params.ENV}"
					echo "Version selected is ${params.VERSION}"
					sh 'printenv'
					myfn()
					mysumfn(3,3)
					}
			}
		}
	}
}
