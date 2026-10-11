# DBMS College Practicals — MySQL

A practical repository based on the supplied `Practicals.pdf`. It covers the College database schema, sample data, 25 prescribed SQL queries, and database administration examples.

## Requirements

- MySQL 8.0 or newer (recommended)
- MySQL Workbench, command-line client, or another MySQL client

## Repository structure

```text
dbms-college-practicals/
├── README.md
├── .gitignore
└── sql/
    ├── 01_create_database.sql
    ├── 02_create_tables.sql
    ├── 03_insert_sample_data.sql
    ├── 04_practical_queries.sql
    └── 05_database_administration.sql
```

## Run the project

Run these files in order on a test database:

1. `sql/01_create_database.sql`
2. `sql/02_create_tables.sql`
3. `sql/03_insert_sample_data.sql`
4. Run individual queries from `sql/04_practical_queries.sql`
5. Run selected commands from `sql/05_database_administration.sql` only if you have the required privileges.

### Important safety notes

- The query file includes `UPDATE` and `ALTER TABLE` statements that change data/schema. Run on a test database or take a backup first.
- Q7 changes the name for roll number `X2001`.
- Q18 increases all course seat counts by 10%.
- Q19 and Q23 add columns. Re-running those statements without resetting the schema will fail because the columns already exist.
- Q20 changes every admission date by one year. Do not run it repeatedly unless that is intended.
- The administration file creates users/roles and contains privileged commands. Replace placeholder passwords before use; never commit real credentials.
- The sample data intentionally leaves one student without an admission, one course without students, and one society without members so outer-join and `NOT EXISTS` examples can be tested.

## Notes

- The scripts target MySQL 8.0+. Some syntax differs in SQLite or other database engines.
- In the source PDF, the course type diagram abbreviates values as `F / P`, while the DDL and sample queries use `Fulltime` and `Parttime`. This repository follows the DDL/query values.
- `Cname` has a `UNIQUE` constraint, so MySQL creates a unique index for it automatically; no duplicate unique index is created here.
- The SQL scripts are separated for readability. The 25-query file is a practical worksheet and is not intended to be run repeatedly from top to bottom without resetting the database.

## Upload to GitHub

1. Sign in to GitHub and click **New repository**.
2. Give it a name such as `dbms-college-practicals`.
3. Choose **Public** or **Private**, then create the repository.
4. On your computer, extract this project ZIP.
5. Open a terminal in the extracted project folder and run:

```bash
git init
git add .
git commit -m "Add DBMS college practicals"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/dbms-college-practicals.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username and use the repository URL GitHub gives you. Git may ask you to authenticate in your browser.

### Upload without Git (browser)

You can also create a repository on GitHub, choose **Add file → Upload files**, drag in the extracted project files, enter a commit message, and click **Commit changes**.
