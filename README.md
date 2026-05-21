Developer Pushes Code
        ↓
   GitHub Repository
        ↓
   Jenkins Pipeline  (running on AWS EC2)
        ↓
   Maven Build  →  mvn clean package
        ↓
   Docker Image Build  →  docker build
        ↓
   Push to DockerHub  →  docker push
        ↓
   Deploy Container on AWS EC2  →  docker run
