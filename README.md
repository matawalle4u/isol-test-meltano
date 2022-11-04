# Isolated Test Environment Implementation with Meltano and SnowFlake

## Implementation details

The system implementation is to extract data from two snowflake database tables and load into a csv file on the project directory root.
The system uses two isolated environments, **_test environment_** to extract data from snowflake test database, **_prod environment_** to extract data from the snowflake production database.

The system architecture is illustrated in the picture below

![System Architecture](https://github.com/matawalle4u/isol-test-meltano/blob/main/System%20Architecture.png)

## Requirements

- A recent version of [python](https://python.org) programming language (Python version 3.8.10 was used for this article)
- A recent python preferred installer program i.e [pip](https://pip.pypa.io/en/stable/installation/) (pip 22.3 was used for this article)
- You may need to install a python [virtual](https://docs.python.org/3/library/venv.html) environment (It is optional but recommended)
- A recent version of [Meltano](https://docs.meltano.com/getting-started/installation) 


## Installation

- Clone the project repo by running

```bash
git clone https://github.com/matawalle4u/isol-test-meltano.git
```

- Navigate to the cloned folder on your local computer by running

```bash
cd isol-test-meltano
```

- Install Meltano by running

```bash
pip install meltano
```

- Configure the extractor added to use your snowflake account, databases and tables by running

```bash
meltano config tap-snowflake set --interactive
```


## Usage

To use the system follow the instructions below
- Run the command below in your terminal

```bash
meltano --environment=test elt tap-snowflake target-csv
```
You may switch environments by changing the environment in the **_--environment=<new_environment_name>_**


[def]: https://i.imgur.com/uI0hX61.png