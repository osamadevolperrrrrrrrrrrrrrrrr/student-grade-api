بعد فك الضغط افتحي المجلد في VS Code.

1) في pom.xml بدلي:
   YOUR-SONAR-ORG
   YOUR-SONAR-PROJECT-KEY

2) شغلي الاختبارات:
   mvn clean test

3) شغلي التطبيق:
   mvn spring-boot:run

4) افتحي:
   http://localhost:8080/api/students
   http://localhost:8080/api/health

5) ارفعيه GitHub:
   git init
   git add .
   git commit -m "Initial commit: Student Grade API"
   git branch -M main
   git remote add origin https://github.com/YOUR-GITHUB-USERNAME/student-grade-api.git
   git push -u origin main

6) أضيفي أسرار GitHub Actions:
   DOCKERHUB_USERNAME
   DOCKERHUB_TOKEN
   SONAR_TOKEN

7) بعد نجاح Actions شغلي Docker:
   docker pull YOUR-DOCKERHUB-USERNAME/student-grade-api:latest
   docker run -d -p 8080:8080 --name grades YOUR-DOCKERHUB-USERNAME/student-grade-api:latest

8) تأكدي من:
   http://localhost:8080/api/health
   docker logs grades
