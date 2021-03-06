<h2>Apache Airflow for building workflows (Ubuntu server)</h2>
<p>Apache Airflow is the workflow management system to <b>create, schedule and monitor</b> workflows.</p>
<h3>Workflow case study</h3>
<p>Scheduling workflow for scraping webpage for getting currencies rates, processing it with expense data and mailing outcome.</p>
<image src="images/graph.JPG">
<h3>Airflow</h3>
<ul>
  <li>When failure, we can only rerun the part of workflow that was affected.</li>
  <li>DAG - collection of tasks organized in a way that reflects their defined dependencies and relationships.</li>
  <li>While we treat DAG as conatiner for tasks, what triggers certain actions is operator - it says what kind of action we want to perform.</li>
  <li>Task - instantiated operator which describes single task in workflow. Instantiating task requires providing unique task id and DAG container.</li>
</ul>
<h2>Notes</h2>
<h3>Setup on Ubuntu</h3>
<ul>
  <img src="images/airflow-webserver-d.JPG">
  <li>sudo apt install python3-pip</li>
  <li>sudo pip3 install apache-airflow</li>
  <li>airflow initdb</li>
  <li>airflow webserver -p 8080</li>
  <li>airflow webserver -D -->> running airflow in the background</li>
  <li>airflow scheduler -->> in another terminal</li>
  <li>airflow scheduler -D</li>
  <li>localhost:8080/admin</li>
  <li>ctrl + z -->>  stoping command</li>
</ul>
<h3>Useful commnads</h3>
<ul>
  <li>'cd ..' : moving back one directory.</li>
  <li>'ls -l'</li>
  <li>'sudo apt install vim'</li>
  <li>'vim script.py': new file in current directory <br>
       esc ->> ':w'  : write a file <br>
       esc ->> ':wq' : wirte and quit a file <br>
  </li>
</ul>
<h3>Directed Acyclic Graph</h3>
<ul>
  <img src="images/dag.JPG">
</ul>
<h3>Downstream info flow</h3>
<ul>
  <img src="images/downstream.JPG">
</ul>
<h3>DAG files directory</h3>
<ul>
  <img src="images/dag_files_dir.png">
</ul>
