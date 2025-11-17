📢 Notices Board Full Stack Application

Project in this repository was created during ***Design and Implementation of Web Systems*** course throughout my masters degree at Wrocław University of Science and Technology. Additionaly ***Github Actions*** workflows configured in this repository builds both applications (frontend + backend) and creates ready-to-deploy Docker image and pushes it to docker hub. On top of that in backend folder you can also find docker-compose responsible for running monitoring stack.

CI/CD pipeline implemmented in this project helped me prepare case studies for my masters thesis: "Multifaceted comparative analysis of cloud platforms in CI/CD processes using performance-cost criteria" where I compared time, performance and CO2 emissions of different sizes of Virtual Machines available in Microsoft Azure, Amazon Web Services as well as Google Cloud Platform.

## ✨ Technologies

- `Java + Spring Boot (build tool: Maven)`
- `JavaScript + Angular (build tool: npm)`
- `PostgreSQL`
- `Prometheus & Grafana`
- `Docker`
- `GitHub Actions`

## 🚀 Features

- CRUD operations for Notices on the board
- Handling user authentication
- Filtering notices based on criteria (title/description/tags, like/equals/contains)
- Chat between user and Notice owner 
- Monitor several statistics regarding infrastracture usage
- Package frontend and backend applications to images and place them in registry
 
## 🚦 Running the Project

0. Clone the repository

# Frontend
1. Install dependencies: `npm ci` (in frontend folder)
2. Run development server `npm start`
4. Open `http://localhost:4200` in your browser

# Backend
1. Specify your local databse details in application.properties file
1. Build project: ` mvn clean -DskipTests compile package` (in frontend folder)
2. Start server `java -jar target/project-0.0.1-SNAPSHOT.jar`
4. Webserver will be available under link `http://localhost:8080`

# Monitoring
1. Run command `docker compose up` in `backend` folder.
2. Add data source in Grafana
