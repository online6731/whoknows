# Template Manager
Template Manager is a python code which implements the functionality for template pipeline. Template pipeline is the production line of a template. Each template gets created at first state and becomes complete at last state by successfully passing the required operations.


# How to deploy?
Setting up is simple, just follow these steps.

### Python
1. Install python and pip and git:
`apt install git python3 python3-pip`

2. Clone the repository:
`git clone ...`

3. Go to repository folder:
`cd guessit-template-manager`

4. Install dependencies:
 `pip install -r requirements.txt`

5. Start server:
 `python3 app.py`


### Docker
1. Clone the repository:
`git clone ...`

2. Go to repository folder:
`cd guessit-template-manager`

3. Build image from dockerfile:
`docker build -t guessit-template-manager`

4. Run docker image:
`docker run -it guessit-template-manager`


# Main concepts
These are the main concepts of template manager

## Pipeline Functions
Main functions of template manager are the following:

### Duplication Test
> Checks the similarity of given template with all the available templates in database and returns true if there is no similar template

### Acceptance Test
> Checks the votes of testers to see if given template is going to be liked by users or not

### Data Test
> Checks if required data for given template is ready or not

### Schema Test
> Checks the schema of given template to see if all required fields are filled or not

### Generation Test
> Generates sample questions from template to see if the success rate is acceptable or not

###  Manual Test
> tester checks the template and some sample generated questions to see if everything is ok

### Tagging Test
> Checks if template is properly tagged to be used in which contests


## Pipeline States
State shows the situation of template in pipeline. These are the following states in the template pipeline:

### 1. Writing
> Some required fields of template are empty

### 2. Repair
> Template has some problems in generating question

###  3. Ready
> Template is completed and ready for manual test

### 4. Verified
> Template is verified and has no problem of any kind

### 5. In use
> Template is done and can be used in application


# How to use?
Template manager is available via API and CLI

### Test and Save templates
> Gets a template and test it by passing it through the template pipeline and then save the template and save it

API:
- route: /template/test_and_save
- request : { template: Template }
- response : { ok: Bool, template: Template }

CLI:
- command: wtm --run test_and_save --template <template_file_address>

### Search and Get templates
> Gets a mongodb query as condition and returns all templates that  match the condition

API:
-  route: /template/find
- request : { condition: MongoQuery }
- response : { ok: Bool, templates: Template[] }

CLI:
- command: wtm --run find --condition <mongo_query>


# Contributers
- Mohammad Parsian
- Danial Keimasi
- Moein Samadi
