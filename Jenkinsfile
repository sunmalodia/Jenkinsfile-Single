
stage name: 'setup'
node {
    if (isUnix()) {
        echo "unix mode"
	    sh 'pwd'
        sh "ls -la"
    } else {
        echo "windows mode"
        bat "cd"
        bat "dir"
    }
/*
    wrap([$class: 'Groovy']) {
        def script = '''
        println "\n\nSystem Properties"
        System.properties.each { k,v -> println "$k = $v" }
        println "\n\nEnvironment"
        System.getenv().each { k,v -> println "$k = $v" }
'''
    }
*/

    // Testing
}
/*
stage name: 'build'
node {
    if (isUnix()) {
         sh './gradlew clean build'
    } else {
        bat './gradlew.bat clean build'
    }
}
*/
stage name: 'postbuild'
node {
    if (isUnix()) {
        sh 'ls -la'
    } else { 
        bat 'dir'
    }
}
