---
route: nnect-apache-superset
allow_guest: 1
published: 1
---


> **Apache Superset** is an open-source modern data exploration and visualization platform.


1. You need to first generate a database user for your site. Follow this [documentation](https://frappecloud.com/docs/database-users-and-permission-manager) to create a read-only user.


Typically, it takes a few seconds to configure the database user. Once it's complete, click on **View Credential**

![Screenshot 2025-01-31 at 1.15.44 PM](/files/Screenshot 2025-01-31 at 1.15.44 PM.png "Screenshot 2025-01-31 at 1.15.44 PM.png")
2. Open your Superset dashboard and go ahead with connecting a new database.

![Screenshot 2025-01-31 at 2.53.56 PM](/files/Screenshot 2025-01-31 at 2.53.56 PM.png "Screenshot 2025-01-31 at 2.53.56 PM.png")
3. Choose **MySQL** as database type.

![Screenshot 2025-01-31 at 2.54.49 PM](/files/Screenshot 2025-01-31 at 2.54.49 PM.png "Screenshot 2025-01-31 at 2.54.49 PM.png")
4. Fill in all the required details and ensure the **SSL** checkbox is checked. Then, proceed.

![Screenshot 2025-01-31 at 2.56.20 PM](/files/Screenshot 2025-01-31 at 2.56.20 PM.png "Screenshot 2025-01-31 at 2.56.20 PM.png")
5. You will see this message upon a successful connection.

![Screenshot 2025-01-31 at 3.19.46 PM](/files/Screenshot 2025-01-31 at 3.19.46 PM.png "Screenshot 2025-01-31 at 3.19.46 PM.png")
6. Now, you can refer to the [official documentation](https://superset.apache.org/) to create a dashboard in Superset.
