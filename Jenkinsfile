pipeline {
	agent {
        	label '!windows'
    	}
    	environment {
        	DISABLE_AUTH = 'true'
        	DB_ENGINE    = 'sqlite'
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
					sh 'printenv'
					}
			}
		}
	}
}
