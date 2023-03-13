pipeline{
    agent any
    stages{
        stage('Initialize'){
            steps{
                echo """Checked out the codebase to ${WORKSPACE}"""
            }
        }
        stage('DeployKafkaProducer'){
            steps{
                bat """kamel run --config secret:kafka-props ${WORKSPACE}/generic-examples/kafka/sasl_ssl/SaslSSLKafkaProducer.java"""
            }
        }
    }
}