# Tianjin University: Course Design MyLife
## A One-Stop Learning, Social, and Entertainment Platform

Introduction:
In an era marked by information overload and interconnected social networks, there is a pressing need among students for a one-stop platform that addresses learning, socializing, and entertainment. In response, we have developed a comprehensive software tailored for students, aimed at fostering a community that promotes interaction, sharing, and personalized recommendations. This platform integrates a unique movie and music recommendation system and suggests friends with similar interests and personalities.

---

<table>
  <tr>
    <th>Programming Languages and Development Frameworks</th>
    <th>Front-end Technologies</th>
    <th>Database Technologies</th>
  </tr>
  <tr>
    <td>
      <div>
        <a href="https://www.python.org/">
          <img src="https://img.shields.io/badge/Python-v3.9.18-3776AB?style=flat&logo=Python" alt="Python">
        </a><br>
        <a href="https://www.javascript.com/">
         <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&color=grey" alt="JavaScript">
        </a><br>
        <a href="https://www.djangoproject.com/">
          <img src="https://img.shields.io/badge/Django-v4.1-092E20?style=flat&logo=Django" alt="Django">
        </a>
      </div>
    </td>
    <td>
      <div>
        <a href="https://www.w3.org/TR/html5/">
          <img src="https://img.shields.io/badge/HTML-5-E34F26?style=flat&logo=HTML5" alt="HTML">
        </a><br>
        <a href="https://getbootstrap.com/">
          <img src="https://img.shields.io/badge/Bootstrap-v5.3.2-7952B3?style=flat&logo=Bootstrap" alt="Bootstrap">
        </a><br>
        <a href="https://jquery.com/">
          <img src="https://img.shields.io/badge/jQuery-v3.7.1-0769AD?style=flat&logo=jQuery" alt="jQuery">
        </a>
      </div>
    </td>
    <td>
      <div>
        <a href="https://www.mysql.com/">
          <img src="https://img.shields.io/badge/MySQL-v8.0.35-4479A1?style=flat&logo=MySQL" alt="MySQL">
        </a><br>
        <a href="https://redis.io/">
          <Strong>TODO:</Strong><img src="https://img.shields.io/badge/Redis-version-DC382D?style=flat&logo=Redis" alt="Redis">
        </a>
      </div>
    </td>
  </tr>
</table>

## User Guide

**Starting a Django Project**:

- First, make sure you are in the project directory.

- Open the command line interface (Windows users use `Anaconda Prompt`, Mac users use `Terminal`).

- Use the command `python manage.py runserver` to start the development server, which by default launches the Django app at `http://127.0.0.1:8000/`.

- To launch the server on a different port, specify the port number, such as: `python manage.py runserver 8080`.

- To access your development server from other machines on the network, use `0.0.0.0:8000` (or another port number) as the address. For example: `python manage.py runserver 0.0.0.0:8000`.

  > Note! This action allows external access to your development server and poses a security risk.

**Ending a Django Project**:

- To stop the server, press <kbd>Ctrl</kbd>+<kbd>C</kbd> in the command line interface.

- If the server does not stop correctly, find the Python process in the command line and force it to end.

  - On Windows, find the relevant Python process in the Task Manager and end it.

  - On Mac, use the `Activity Monitor` or the `kill` command in the command line.

## Django Project Setup Method

1. **(Recommended) Install Anaconda**

   - Visit the official Anaconda website: [www.anaconda.com](https://www.anaconda.com) and download the installer from the [download page](https://www.anaconda.com/download).
   - If in **Mainland China**, due to network issues, it is recommended to use the [Tsinghua University Anaconda mirror site](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/) for the download.
   - After installation, follow [this tutorial(in Chinese)](https://blog.csdn.net/weixin_43914658/article/details/108785084) to configure the environment variables to ensure Anaconda can be run from the command line.

2. **Enter the Project Directory**
   
   - Use the command line interface to navigate to your project folder.
   
3. **Create and Activate a Virtual Environment**
   - To create a virtual environment, enter the following command in the command line:
     ```bash
     conda create -n MyLife_env python=3.9.18   # “MyLife_env” is the name of the virtual environment, which can be changed to your preference
     ```
   - To activate the virtual environment:
     ```bash
     conda activate MyLife_env   # Make sure to use the name of your chosen virtual environment
     ```

4. **Install Project Dependencies**

   - Install dependencies using pip. In the project directory, there is a [`requirements.txt`](./requirements.txt) file listing all the necessary Python libraries.

     First, check if you are in the correct environment:

     ```bash
     where pip   # Windows
     which pip   # MacOS
     ```

     This command will display the path of the `pip` command. Ensure the output path is pointing to the `pip` in your virtual environment (`MyLife_env`), then use the following command to install the dependencies:

     ```bash
     pip install -r requirements.txt
     ```

   - If in **Mainland China**, consider using the [Tsinghua University PyPI mirror](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/) to speed up the installation of dependencies:
     ```bash
     pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
     ```

5. **Database Initialization**

   - Visit the official MySQL website [https://www.mysql.com](https://www.mysql.com), [download](https://dev.mysql.com/downloads/mysql/) and install MySQL, and set your password.
   - Log in to MySQL:

     ```bash
     mysql -u root -p   # mysql --user {username} --password {password}
     ```

   - Create the `MyLifeDB` project database in MySQL

     ```sql
     CREATE DATABASE MyLifeDB;
     ```
