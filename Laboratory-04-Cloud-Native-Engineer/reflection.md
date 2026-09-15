
### 1. How does the boot time and setup process of a Docker container compared to installing an operating system on a Virtual Machine?
Containers start up almost instantly in just a few seconds compared to Virtual Machines, which can take several minutes because they have to boot an entire operating system. Since Docker containers share the host computer's 
main engine and only run the app itself, they use way less RAM, CPU power, and storage space than heavy virtual machine setups.

### 2. Why is port mapping (-p 8080:80) necessary when running a web server inside a container?
Port mapping is necessary because containers live inside their own closed network by default. Using the `-p 8080:80` setting acts like a simple bridge: it sends web traffic coming into port 8080 on my real machine
straight into port 80 inside the container so outside users can actually open and view the NGINX web server.

### 3. What happens to the data inside a container when you use the docker rm command?
Running docker rm completely deletes the container along with any unsaved data stored inside it. This shows that containers are temporary by design—they are built to be easily created, stopped, wiped out, and replaced without leaving mess on the main machine, unless you link them to extra outside storage.

### 4. How do you think containerization changes the way software developers and IT operations teams work together (DevOps)?
Containerization makes it much easier for coders and system admins to work as one team. By putting an app and everything it needs into one Docker container image, it fixes the old problem where code works 
on a developer's computer but breaks somewhere else. Both teams can now run the exact same setup smoothly.

### 5. How is your GitHub portfolio evolving?
My GitHub portfolio is growing from basic setup work into a real showcase of practical cloud skills. Adding terminal commands, uploading proof screenshots, and writing clean notes shows that I am getting
better at managing modern cloud systems and container tools step by step.
