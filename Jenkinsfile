pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git-branch:'master',url:'https://github.com/Hemanthd5/MyMaven111'
}
}
stage('Build'){
steps{
sh 'mvn clean package'
}
}
stage('Test'){
steps{
sh 'mvn test'
}
}
stage('Run Application'){
steps{
sh 'java -jar target/MyMaven11-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo 'Build and deployment successfull'
}
failure{
echo 'Build failed'
}
}
