## Welcome to MY Data science project learning journal

# Self-intro

On 2020 Nov 28, I decided to try my best to land in data science area. There were 2 triggers: one was I felt I was going to be fired, which was pros significently outweighted cons. The 2nd was a private DS training based on a algo trading project from Dec 2 to end of March 2021 and I would have time to follow this training. (syllabus: https://docs.google.com/presentation/d/12eQu5zkDkui7iwZMovxsOZQOLSZ1hQy-TmyQZBnkGpQ/edit#slide=id.p10. I brought www.datacamp.com with the black friday discoun and used it for me to lay the DS fundation in Python, statistic etc. (My sql was already ok)

Today I found this: a project for Financial Investment Risk Management. https://medium.com/learn-from-machines/part-0-project-description-7f74ff7aae78 The mission is divided into DATA ENGINEERING/DATA SCIENCE/MACHINE LEARNING/INVESTMENT RISK MANAGEMENT. It is much difficult to become a data scientist from 0 to 1. Honestly, The most regetable thing in my life would be if I could not have a great career path (even worse than die alone). I believe do some projects is needed to get myself employable/job-ready in DS, and this one looks good. **Bold** Feel free to inform me anything you feel could help me to be a better man which means dont have to be DS or IT professional related things.

# PART 0 Some initials

1. GitHub page - this blog for me to be known

2. Install Windows Subsystem for Linux (WSL)
https://docs.microsoft.com/en-us/windows/wsl/install-win10

3. Install Ubuntu

# PART 1 Docker

0. Learn how to install docker in Ubutu familiar commands

1. Understand the concept and familiar usage of WSL+Ubuntu+Docker for windows
this video helped me really understand relationships with WSL/Ubuntu/Docker
https://www.youtube.com/watch?v=5RQbdMn04Oc(PS: that budy got a really awsome room!)
some basic commands explaination:
https://www.youtube.com/watch?v=HqBMEmoAd1M&ab_channel=AutomationStepbyStep-RaghavPal
docker pull 
docker images
docker rmi ## Remove all images
docker stop 
docker run --name dockername
docker rm <container_id>##Remove containers
docker build -t
docker ps -a


# PART 2 Install Postgres on the Docker
https://medium.com/learn-from-machines/part-2-install-postgresql-on-a-docker-image-84e6cceba9b9

docker pull postgres ##get the image
docker run --name cont_postgres -e POSTGRES_PASSWORD=*** -d postgres:13.0-alpine  ***haven't figure out how to correctly add --volume $HOME/Desktop/FRM_project/volumes/postgres:/var/lib/postgresql/data img_postgres

sudo docker exec -it cont_postgres bash
psql -h localhost -d postgres -U postgres ### come into the commandline for the DB

CREATE USER steve WITH ENCRYPTED PASSWORD 'yourpass';
create database frm_db_dev;
GRANT ALL PRIVILEGES ON DATABASE frm_db_dev TO steve;

##relog in the db using 'steve'
\q
psql -h localhost -d db_name -U steve
sudo docker start cont_postgres
sudo docker exec -it cont_postgres psql -d db_name -U steve

This video clearly illustrats 'Install PostgreSQL on a Docker'
https://www.youtube.com/watch?v=aHbE3pTyG-Q&ab_channel=Amigoscode

You can use the [editor on GitHub](https://github.com/steveding1/steveding1.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/steveding1/steveding1.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
