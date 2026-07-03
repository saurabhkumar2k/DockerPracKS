# DockerPracKS
**Docker Concepts**
1. Private repository created.
   <img width="1888" height="766" alt="image" src="https://github.com/user-attachments/assets/c583a17e-655e-43b7-82f6-3a7a0562ee76" />
2. An authentication token and authenticate your Docker client to your registry.
   <img width="1187" height="402" alt="image" src="https://github.com/user-attachments/assets/670de9af-2162-444e-ac90-a8bd295ff22d" />
3. Build Docker image using the following command :docker build -t kumarsaurabh/travelmemory .
   <img width="1088" height="443" alt="image" src="https://github.com/user-attachments/assets/c71ca3cb-d826-4e09-be68-3496f391491c" />
4. tag docker image so that image can be pushed to this repository
   <img width="1252" height="322" alt="image" src="https://github.com/user-attachments/assets/80cf86f8-c0c0-4c46-8539-869276ca3ec1" />
5. Now push this image to your newly created AWS repository;
   <img width="1157" height="452" alt="image" src="https://github.com/user-attachments/assets/cee79502-b5c4-4359-a98b-8a38d0e0ace5" />
6. Check for the docker images.
   run a command docker image list
   <img width="1040" height="256" alt="image" src="https://github.com/user-attachments/assets/ac82beee-46fb-4337-95bc-bf15425d5b07" />

**Docker Composer**
1. Created two services named ms1 and ms2.
2. Put app.py file indivisually in both of the services with different return messages as under
   <img width="643" height="347" alt="image" src="https://github.com/user-attachments/assets/c43d7963-7de5-4a47-98a6-f88a92e93719" />
3. Now docker-compose.yml is being introduced to the application with sample code snipped like:
   services:
       app1:
       build:
         context: ./ms1
         dockerfile: Dockerfile
       image: b17bflasksamplems1:v1
       container_name: b17-flask-app-ms1
       ports:
         - "5001:5000"

    # depends_on:
       #   - app2
     app2:
       build:
         context: ./ms2
         dockerfile: Dockerfile
       image: b17bflasksamplems2:v1
       container_name: b17-flask-app-ms2
       ports:
         - "5002:5000"
<img width="997" height="412" alt="image" src="https://github.com/user-attachments/assets/0815f828-7fe7-4d32-9a97-a4eb949f7228" />
4. Use command "docker compose build" to run both of the applications i.e ms1 and ms2.
   <img width="945" height="402" alt="image" src="https://github.com/user-attachments/assets/c8602249-ea9d-4219-b852-456aa3f54172" />




