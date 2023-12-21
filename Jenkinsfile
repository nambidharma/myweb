pipeline {
	agent any 
	stages {
		stage("working with file operations") {
			steps {
				script {
					File file = new File("/tmp/file1.txt")
					println file.readLines()
					for(line in file.readLines()){
						println line
					}
				}
			}
		}
	}
}
