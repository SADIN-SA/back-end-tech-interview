# Project Describtion

This project is part of the **Back-End Developer Interview Test**.  
The goal is to create project simulates a simple IoT data management system.
It includes a front-end (for interaction), an API (for data management), a PostgreSQL database (for persistence), and a background service (to handle incoming telemetry data).
A device emulator will simulate real IoT devices sending telemetry data.

---

## Tasks

**Step 1:** Review and Planning (24 hours)

You will have 24 hours to review the task and prepare your approach before starting development.

This step allows you to understand the scope and plan your solution carefully.
Since protocols such as MQTT are not widely used outside the IoT field, take your time to review them if needed.

At the end of this 24-hour period, it will be a **plus** if you share a short plan that includes:

1. ER Diagram – showing database structure
2. List of APIs – showing endpoints and their purpose
3. System Diagram – showing how components interact

These are not mandatory but will help demonstrate your understanding and planning skills.

**Step 2**: Implementation (24 hours)

After completing your plan, you will have another 24 hours to implement the project.

please follow this structure:
```
< project-repo >/
├── front-end/
│    └── < front-end implementation >
├── api/
│    └── < api implementation >
├── service/
│    └── < telemetry service implementation >
├── device_emulatour/
│    ├── .env.example             # example of env vars 
│    ├── device_emu.py            # logic of emulator
│    ├── dockerfile               # dockerazition of the emulator
│    ├── requirments.txt          # needed library
│    └── run.sh                   # simple script to run the docker of emulator 
├── README.md                     # Project usage instructions + documentation
└── PROJECT_TASK.md               # The task description file
```


Once submitted, your code will be reviewed.
The goal of the review is to ensure you understand what you built and did not rely entirely on AI-generated solutions.
You will receive feedback to help clarify expectations and evaluate your understanding, logic, and coding standards.

### Deliverables

1. -[ ] Source code (front-end, API, and service)

(Optional but recommended) Planning deliverables:

1. -[ ] ER Diagram
2. -[ ] API List
3. -[ ] System Diagram

## Project detailes

### 1. Front-End (Plain HTML)

Create simple HTML pages for:

1. **Login Page**
2. **User CRUD Page**
3. **Device CRUD Page**
4. **Telemetry Page**
   - Display:
     - Device Name  
     - Timestamp  
     - Value  
     - Key

### 2. API (Flask)

Implement a Flask API with the following features:

1. **Authentication**
   - JWT-based authentication

2. **User CRUD**
   - Fields:
     - `email`
     - `username`
     - `password`

3. **Device CRUD**
   - Fields:
     - `id`: UUID
     - `name`
     - `created_at`
     - `created_by`

4. **Telemetry API**
   - Fields:
     - `device_id`
     - `value`
     - `key`
     - `timestamp`

### 3. Database (PostgreSQL)

Use PostgreSQL to store:

- Users  
- Devices  
- Telemetry  


### 4. Service

Implement a background service that:

- Receives telemetry messages  
- Stores them in the database  

### 5. Device Emulator (Provided)

The device emulator is already implemented.

- Device IDs are defined in the `.env` file  
- Sends telemetry to the following topic:

