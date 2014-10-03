# DSSG/DSaPP Project Template
--------

Or, How to build *data science* projects that can be rerun. This is an opinated templated produced by [Hunter Owens](http://hunterowens.net) and [Carl Shan](http://www.carlshan.com/) on behalf of the [Center for Data Scienece and Public Policy](http://harris.uchicago.edu/content/center-data-science-and-public-policy-0). The idea for a project template is heavily inspired by the NPR apps team's [project template](http://harris.uchicago.edu/content/center-data-science-and-public-policy-0). 

## Using

To create a project using this as a template-

1. Create a new repository on Github without a README or LICENSE file. 
2. Clone the repository to your local machine. 
3. Run `git remote add upstream https://github.com/dssg/project_template.git`. This adds the template repo as a remote that you can pull from. 
4. Run `git pull upstream master`. Pull in all the commits on the template to the current master branch. 
5. Run `git push origin master`. Push the template to the github master branch. 
6. Replace README.md with one appropriate for your project. 
7. Profit!

###Key Concepts

`requirements.txt` should be a text file that contains all the python packages required for this project to be run. 

`build.sh` is a shell script that should run your ETL, Run the models and then validate them. *This may be replaced by [Drake](https://github.com/Factual/drake) or Makefiles in the future*. 

`etl` is the directory in which you should have scripts that take data from your source of truth (typically raw data that has been uploaded to an S3 bucket) and loads it into a Data Warehouse (typically Postgres). It may contain subdirectories for projects that have multiple data sources. For example, an project could have a script/sub-directory for each school distract that provides data. 

`exploration` is directory in which visualizations and exploration of the data is preformed. If you are using iPython Notebook, this is where you should put all of your notebooks. If you need to build assets (ie, charts) as part of your build pipeline, you may include stuff from this directory as part of your build pipeline (see above), but typically, is is avoided. 

`model` is the directory in which all statistical models live. 

`validation` is the directory in which you preform model validation. 


## Assumptions

## Conventions




  