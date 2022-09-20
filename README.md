<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">Ansible reporting with ARA: Ansible Run Analysis</h3>
  <p align="center">
    Detailed analysis of the Ansible playbook runs
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#prerequisites">Prerequisites</a>
      <ul>
        <li><a href="#SQLite">SQLite 3.8.3</a></li>
        <li><a href="#Python">Python 3.8</a></li>
      </ul>
    </li>
    <li><a href="#Recording_playbooks">Recording playbooks</a></li>
  </ol>
</details>

## About The Project

For RHEL 7 and CentOS 7 it is recommended to install python3.8 due to missing or outdated dependencies. 
It provides you with a detailed analysis of your Ansible playbook runs, which includes:
•	Tasks description, status and output
•	Play description and duration
•	Hosts involved
•	Files executed
•	Parameters used

Use the `README.md` to get started.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Prerequisites

### SQLite 3.8.3

#### Upgrading SQLite on CentOS to 3.8.3 or Later
Download the source code from https://www.sqlite.org/download.html
* sqlite
  ```sh
  cd /opt
  wget --no-check-certificate https://www.sqlite.org/2022/sqlite-autoconf-3390300.tar.gz
  ```
* Extract File
   ```sh
  tar -xvf sqlite-autoconf-3390300.tar.gz
  cd sqlite-autoconf-3390300
  ```
 * Compile
    ```sh
   ./configure
   make
   make install
   echo “export LD_LIBRARY_PATH=/usr/local/lib” >> /root/.bashrc
   ```
 Checking SQlite3 version quickly
   ```sh
  python3.8 -c "import sqlite3; print(sqlite3.sqlite_version)"
  ```
