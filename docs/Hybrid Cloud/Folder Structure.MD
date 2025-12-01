---
route: folder-structure
allow_guest: 1
published: 1
---

* All the Agent related configs will be in an ``` agent ``` folder in the frappe user
* The Benches will be in a ``` benches ``` directory under the frappe user. These doesn’t have the complete capabilty of a frappe bench.
* All the archived benches will be in the ``` archived ``` folder
* The ``` frappe ``` user’s UID and GID should be 1000:1000
* There will be docker containers which are actually the benches and will have complete access to bench commands

![](/files/Screenshot%202023-05-29%20at%202.23.57%20PM.png)

Here is the folder structure inside the ``` benches ``` directory

![](/files/Screenshot%202023-05-29%20at%202.25.28%20PM.png)

Accessing Bench commands can only be done from within the container

![](/files/Screenshot%202023-05-29%20at%202.27.16%20PM.png)
