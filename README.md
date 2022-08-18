## DAACS Summary Report Shiny Application


### Installation


```{bash, eval=FALSE}
sudo apt-get update
sudo apt-get install pandoc
```

```{r, eval=FALSE}
install.packages(c('mongolite', 'tidyverse', 'psych', 'shiny', 'rmarkdown', 'readxl', 'knitr')
```


Create a configuration file in the `config/` directory.

```{r, eval=FALSE}
login.message <- "This is a prototype of the DAACS Advisor Dashboard. Please contact admin@daacs.net for access."

colors <- c('#1f78b4', '#b2df8a', '#33a02c')

LOCAL_DB <- FALSE
local.db <- 'daacs_cache.rda'

mongo.host <- 'my.daacs.net'
mongo.port <- 27017
mongo.db <- 'daacsdb'
mongo.collection.users <- 'users'
mongo.collection.assessments <- 'user_assessments'
mongo.collection.events <- 'event_containers'
mongo.user <- 'DB_USER'
mongo.pass <- 'DB_PASSWORD'

daacs.base.url <- paste0('https://', mongo.host)

# Whether the dashboard should display raw scores (as percentages) or as levels
# (i.e. developing, emerging, mastering)
scores.raw <- FALSE
```
