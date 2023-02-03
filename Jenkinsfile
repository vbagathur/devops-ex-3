---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: jenkins
spec:
  replicas: 1
  selector:
    matchLabels:
    app: jenkins
  template:
    metadata:
    labels:
      app: jenkins
    spec: null
    containers:
      - name: jenkins
  image: 'jenkins/jenkins:latest'
  ports:
    - containerPort: 8080
  volumeMounts:
    - name: jenkins-home
      mountPath: /var/jenkins_home
  volumes:
    - name: jenkins-home
      emptyDir: {}
