# Isolated Test Environment Implementation with Meltano ElT

## Implementation details

The system implementation is to extract data from two snowflake database tables and load into a csv file on the project directory root.
The system uses two isolated environments, **_test environment_** to extract data from snowflake test database, **_prod environment_** to extract data from the snowflake production database.

The system architecture is illustrated in the picture below

![System Architecture](https://i.imgur.com/uI0hX61.png)

## Installation
- Install meltano by running the command below in your terminal

```bash
pip install meltano
```
- Create a meltano 

## Usage

To use the system follow the instructions below
- Run the command below in your terminal

```bash
meltano --environment=test elt tap-snowflake target-csv
```
You may switch environments by
