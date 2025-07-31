# Demo Video Link :


# Document-management-System
🔐 Full-stack Document Management System with JWT auth, role-based access (Admin/Editor/Viewer), document upload/edit/versioning, real-time comments (WebSockets), search &amp; filters, and activity logs. Built with React, FastAPI, Docker, and MySQL. Frontend &amp; backend run via Docker or local dev.


# Steps to Run Both Frontend and Backend Together

Prerequisites:
•	Docker Desktop
•	Optional: Node.js + npm (if you want to run the frontend separately)

A] Steps to run backend docker image:
1.	Clone the GitHub Repository in 
•	git clone https: https://github.com/vaishnaviigitte/Document-management-System.git

2.	Pull the Docker Image from Docker Hub
•	docker pull yashi1803/dms_app_image:latest

3.	Create/Edit the .env File (if not already present)
🔒 This file provides the database credentials to Docker.

4.	Create the MySQL User (appuser)  
✅ This allows FastAPI to connect to MySQL using appuser.

5.	Navigate to the root directory
•	cd \Docker-DMS

6.	Build and Run the Project Using Docker Compose
•	docker-compose up –build
This command will:
	Build the FastAPI backend Docker image
	Start the MySQL database container
	Connect them internally
	Expose FastAPI at: http://localhost:8000

✅ MySQL is ready!
INFO:     Uvicorn running on http://0.0.0.0:8000

7.	(Optional) Enter the MySQL Container to View Data
•	docker exec -it mysql_db mysql -uappuser -papppassword123 document_db
Then run:
•	SHOW TABLES;
•	SELECT * FROM users;
•	SELECT * FROM documents;


B] Steps to run frontend code: 
1.	Clone the Repositor
•	cd FullStack-DMS
  cd dashboard

2.	Install Dependencies
•	npm install

3.	Start the Development Server
•	npm run dev

4.	Access the App
(Open your browser and go to):  http://localhost:5173/
The Document Management System(DMS) UI should now be running locally!



