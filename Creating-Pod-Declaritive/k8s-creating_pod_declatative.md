🔹 YAML Structure

🟢 1. API & Object Type
apiVersion: v1
kind: Pod
apiVersion → which Kubernetes API to use (v1 = basic/core)
kind → type of resource (Pod)

🟢 2. Metadata (Identification)
metadata:
  name: firstpod
  labels:
    app: frontend
name → unique Pod name
labels → tags for grouping and identification
app: frontend → used later by other resources (like Service)

🔵 3. Spec (Actual Configuration)
spec:
Defines what Kubernetes should run

🔵 4. Container Definition
containers:
  - name: nginx
    image: nginx:latest
containers → list of containers inside Pod
name → container name
image → Docker image to run (nginx:latest)

🔵 5. Port Configuration
ports:
  - containerPort: 80
App inside container runs on port 80
❗ Only internal (not exposed outside)

🔵 6. Environment Variables
env:
  - name: USER
    value: "username"
Defines environment variable inside container
USER = username