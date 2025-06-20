## **Deploy WordPress on an EC2 instance, and connect it to an RDS MySQL database for storing data.**

### **Step 1: Create a Security Group for RDS**

   1. Go to VPC > Security Groups
   2. Create a security group called rds-sg
   3. Allow MySQL/Aurora (Port 3306) from EC2’s security group

### **Step 2: Launch an RDS MySQL Instance**

   **1. Go to RDS > Databases > Create database**
   
   **2. Choose:**
      
      * Engine: MySQL
      * Edition: Free tier
      * Instance type: db.t3.micro
      * DB instance identifier: wordpress-db
      * Master username: admin
      * Master password: (Note it down)
        
   **3. Connectivity:**
      
      * Choose default VPC
      * Select the rds-sg you created
      * Public access: Yes (for testing only, not for production)
     
   **4. Create the database and wait till it’s Available**

