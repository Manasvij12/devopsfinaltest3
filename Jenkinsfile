pipeline{
agent any
tools{
maven 'Maven'
jdk 'JDK'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/Manasvij12/devopsfinaltest3.git'
}
}
stage('build'){
steps{
sh 'mvn clean package'
}
}
stage('test'){
steps{
sh 'mvn test'
}
}
stage('run'){
steps{
sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
}
}
}
post{
success{
echo 'build done'
}
failure{
echo 'build failed'
}
}
}

