# PySpark Jupyter Notebook Project

This project contains PySpark Jupyter notebooks for analyzing energy consumption data. You can run this project in two ways:

1. Using Docker (Recommended): This method is guaranteed to work and ensures a consistent environment.
2. Using requirements.txt (Optional): This method is not guaranteed to work and depends on your local system configuration.

---

### Option 1: Using Docker (Recommended)

#### Prerequisites
- Docker installed on your system. If you don't have Docker, follow the installation guide for your operating system:
  - Windows: https://docs.docker.com/desktop/install/windows-install/
  - macOS: https://docs.docker.com/desktop/install/mac-install/
  - Linux: https://docs.docker.com/engine/install/

#### Steps to Run the Project
1. Extract the files from the folder I sent you to a directory on your computer. For example:
   - On Windows: Extract to `C:\Users\<YourUsername>\Documents\pyspark-project`.
   - On macOS/Linux: Extract to `/home/<YourUsername>/pyspark-project`.

2. Open a terminal (Command Prompt on Windows, Terminal on macOS/Linux) and navigate to the extracted folder. For example:
   - On Windows:
     ```
     cd C:\Users\<YourUsername>\Documents\pyspark-project
     ```
   - On macOS/Linux:
     ```
     cd /home/<YourUsername>/pyspark-project
     ```

3. Pull the PySpark Jupyter Docker image:

```
docker pull jupyter/pyspark-notebook:latest
```

4. Run the Docker container and mount the current directory:

```
docker run -p 8888:8888 -v "$(pwd)":/home/jovyan/work jupyter/pyspark-notebook
```

5. Access Jupyter Notebook:
- Open your browser and navigate to `http://localhost:8888`.
- The token for access will be displayed in the terminal where you ran the `docker run` command.

6. Open and run the notebooks:
- In the Jupyter interface, navigate to the `work` directory.
- Open and run the notebooks.

---

### Option 2: Using requirements.txt (Optional)

#### Prerequisites
- Python 3.8 or higher.
- Java 8 or higher (required for PySpark).
- pip (Python package manager).

#### Steps to Run the Project
1. Extract the files from the folder I sent you to a directory on your computer.

2. Open a terminal and navigate to the extracted folder.

3. Install dependencies:

```
pip install -r requirements.txt
```

4. Start Jupyter Notebook:

```
jupyter notebook
```

5. Open and run the notebooks:
- In the Jupyter interface, navigate to the `root` directory (if applicable).
- Open and run the notebooks.

---

### Notes
- Docker is the recommended method as it ensures a consistent environment and avoids dependency conflicts.
- If you choose the requirements.txt method, ensure Java is installed and properly configured. PySpark requires Java to run.
- If you encounter any issues, check the PySpark installation guide: https://spark.apache.org/docs/latest/api/python/getting_started/install.html

---

### Data Files
- The data files used in this project are located in the `work` directory (if applicable).
- Ensure the paths to the data files in the notebooks are correct.

