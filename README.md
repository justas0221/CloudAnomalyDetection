# Cloud Anomaly Detection

This project is an implementation of anomaly detection in network traffic using the NSL-KDD dataset, deployed on an **AWS EC2 instance** for cloud-based analysis.

## Security Best Practices Implemented

To ensure the security of the **AWS EC2 instance**, several best practices were followed:

### 1. **Multi-Factor Authentication (MFA)**
   - **MFA** was enabled for both the root user and IAM users to add an extra layer of security.
   - This prevents unauthorized access even if login credentials are compromised.

   ![MFA Enabled](1.png)

### 2. **IAM Role and Least Privilege Principle**
   - An **IAM user** was created with administrative privileges instead of using the root account.
   - The IAM user was assigned to an **Administrator group** with controlled access.

   ![IAM Administrator Access](2.png)

### 3. **SSH Key-Based Authentication**
   - Used an **SSH key pair** instead of password-based authentication for secure access.
   - This prevents brute-force attacks on the instance.

### 4. **Security Groups and Firewall Rules**
   - **Inbound rules** were configured to allow SSH access **only from a trusted IP address**.
   - Only necessary ports were opened to minimize attack surface.

### 5. **Regular Updates & Patching**
   - Ensured that all installed packages and system software were updated regularly.

### 6. **CloudWatch Logging & Monitoring**
   - Configured **CloudWatch** to monitor system logs and detect any unusual activity.

---

## Dataset Information

The **NSL-KDD dataset** is used for training and evaluating network intrusion detection systems (NIDS). The dataset consists of labeled network traffic data.

### Files Used:
- **KDDTrain+.txt** → Training dataset
- **KDDTest+.txt** → Testing dataset
- **Field_Names.csv** → Column names for the dataset

---

## How to Run

### **1. Clone the Repository**
```bash
git clone https://github.com/justas0221/CloudAnomalyDetection.git
cd CloudAnomalyDetection
```

### **2. Start the Virtual Environment**
```bash
source AnomalyVenv/bin/activate
```

### **3. Launch Jupyter Notebook**
```bash
jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser --allow-root
```

### **4. Access Jupyter Notebook**
- Open a web browser and paste one of the provided links.
- Start exploring the dataset and running anomaly detection models.
