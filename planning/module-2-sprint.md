# Module 2: Sprint 1 implementation notes

The five Sprint 1 stories are implemented and closed through pull requests [#16](https://github.com/KaustubhMukdam/devops-capstone-project/pull/16), [#17](https://github.com/KaustubhMukdam/devops-capstone-project/pull/17), [#18](https://github.com/KaustubhMukdam/devops-capstone-project/pull/18), [#19](https://github.com/KaustubhMukdam/devops-capstone-project/pull/19), and [#20](https://github.com/KaustubhMukdam/devops-capstone-project/pull/20). For each API story, tests were added and observed failing before the route was implemented. The final run passed 29 tests with 96% service coverage and zero Flake8 findings.

The local Windows environment uses Python 3.9 in `.venv` and a PostgreSQL 16 Docker container on port 5432. The course's `bin/setup.sh` is for its Linux Cloud IDE; it was not run on Windows. To run the service locally after dependencies and PostgreSQL are available:

```powershell
$env:FLASK_APP = 'service:app'
.\.venv\Scripts\python.exe -m flask db-create
.\.venv\Scripts\nosetests.exe
.\.venv\Scripts\python.exe -m flask run --host 127.0.0.1 --port 5000
```

The `db-create` command drops and recreates tables, so use it only for a disposable development database. The live CRUD demo is recorded in [Module 2 evidence](../submission-evidence/module-2.md).

## Retrospective

- The test-first cycle caught missing routes and an incorrect create `Location` header before implementation. Separate branches and pull requests kept each story reviewable.
- The starter CLI test passed command-line arguments into Click when run through Nose; explicitly supplying an empty argument list fixed it. Package downloads from the default index were slow, and the Windows environment required a local setup path.
- For the next sprint, run tests and quality checks in GitHub Actions and capture board screenshots at each status transition. The browser surface was unavailable to this session, so the user captured the GitHub board.
