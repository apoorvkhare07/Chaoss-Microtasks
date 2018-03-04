# Reporting of CHAOSS Metrics

## Microtask Submission. 

 *__Requirements__*: 
 1. Basic python development enviroment : virtualenv, python 3, pip3.
 2. GrimoireLab packages, ElasticSearch and mariaDB.  
 3. Elasticsearch should be running on [localhost:9200](http://localhost:9200)
 4. Kibana can also be used in order to visualize data in better way.
										 

*__Problem Statements__*

**Microtask 1**: Produce a listing of the number of new committers per month, and the number of commits for each of them, as a                  table and as a CSV file. Use the GrimoireLab enriched index for git.

**Solution**:
The python code for producing the result is in the [Task_1](https://github.com/apoorvkhare07/Reporting-chaoss-Metrics/tree/master/Task_1) directory. It also contains a csv file with the final result.

I have used [p2o.py](https://grimoirelab.gitbooks.io/tutorial/grimoireelk/a-simple-dashboard.html) for data retrieval,enriching data and uploading it to Elasticsearch.

Elasticseacrh api [Elasticsearch_dsl](https://grimoirelab.gitbooks.io/tutorial/python/elasticsearch-dsl.html) for searching and quering data in elasticsearch indices.

Also I have used python libraries like pandas, datetime, calender for visualizing data in form of tables and generaating csv file.

In order to run the script/notebook, download it and replace `repo_url` with the url of the git repo you want to analyse, replace `raw_index' and `enriched_index' with your desired index names and run the script to get the desired result.

I have analysed [grimoirelab's perceval](https://github.com/chaoss/grimoirelab-perceval) repository.

*__Final Output__*

New Commiters each month
![New Commiters each month: ](https://github.com/apoorvkhare07/Reporting-chaoss-Metrics/blob/master/Task_1/commiters_eachmonth.png  ) 

Total number of commits for each user
![Total number of commits for each user: ](https://github.com/apoorvkhare07/Reporting-chaoss-Metrics/blob/master/Task_1/authors.png)

---

**Microtask 2**: Produce a chart showing the distribution of time-to-close (using the corresponding field in the GrimoireLab                    enriched index for GitHub issues) for issues already closed, and opened during the last six months.
               
---
 
**Microtask 3**: Produce a listing of repositories, as a table and as CSV file, with the number of commits authored, issues opened, and pull requests opened, during the last three months, ordered by the total number (commits plus issues plus pull requests).

---

**Microtask 4**: Perform any other analysis you may find interesting, based on GrimoireLab enriched indexes for git and GitHub repositories.
