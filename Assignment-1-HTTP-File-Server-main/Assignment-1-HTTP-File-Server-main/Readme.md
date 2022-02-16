### HTTP File Server

### Instructions:
1. Assigment details are written in the `Assignment 1 HTTP File Server.docx` document
2. Implement your solution in the `main.py` file (Decomposition into separate files is allowed)
3. Use `python 3.X` for this assignment
4. Don't change already existing files except `main.py`, `.gitignore` and `requirements.txt`
5. In case of adding any libraries to the project, also add them to the `requirements.txt` file

### Ho to run tests on linux/ubuntu:
1. Setup DNS records by running: `echo {IP} {VHOST} >> /etc/hosts` for each server entry 
(example: `echo 127.0.0.1 example1.ge >> /etc/hosts`) 
2. Install dependencies: `pip install -r requirements.txt`
3. Run command: `python run.py main.py config.json`

### Ho to run tests in docker:
1. Install docker 
2. Build dockerfile: `docker build -t assignment-1-tester .`
3. Go to assignment project directory and run: 
    * Linux:`docker run -it -v "$(pwd)":/sandbox assignment-1-tester`
    * Windows PowerShell: `docker run -it -v $(PWD):/sandbox assign-1-tester`
    * Windows CMD: `docker run -it -v %cd%:/sandbox assign-1-tester`
4. At this point you can assume that you'r running `Ubuntu 20.04` with all the necessary dependencies installed, to run 
tests multiple times during development it's not necessary to restart the docker, it is able to see all the changes you 
make in the folder (because of `mounting` the folder with this command `-v "$(pwd)":/sandbox`)
5. To start tests run: `python run.py main.py config.json`
6. To exit run: `exit`
7. You can skip build step and instead you can run docker this way: `docker run -it 
-v "$(pwd)":/sandbox kokadva/assignment-1-tester`

### Authors:
* Giorgi Kobiashvili g.kobiashvili@freeuni.edu.ge
* Konstantine Dvalishvili k.dvalishvili@freeuni.edu.ge
* Giorgi Basilaia g.basilaia@freeuni.edu.ge
