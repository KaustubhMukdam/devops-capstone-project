# Module 2: Sprint 1 TDD evidence

Source checklist: local `modules/module-2.pdf`. The user selected the AI-graded submission route. The course's Linux Cloud IDE setup script was not run in this Windows workspace; an equivalent local Python 3.9 virtual environment and PostgreSQL container were used. The live demo ran with `python -m flask run` on `127.0.0.1:5000`.

## Sprint work

| Story | Merged pull request | Final board state | Board screenshot |
|---|---|---|---|
| Setup environment | [#16](https://github.com/KaustubhMukdam/devops-capstone-project/pull/16) | Done, issue closed | [rest-techdebt-done.png](rest-techdebt-done.png) — card title clipped; replace with a focused capture |
| Read account | [#17](https://github.com/KaustubhMukdam/devops-capstone-project/pull/17) | Done, issue closed | [read-accounts.png](read-accounts.png) — clear final board; focused capture pending |
| Update account | [#18](https://github.com/KaustubhMukdam/devops-capstone-project/pull/18) | Done, issue closed | `update-accounts.png` — pending focused capture |
| Delete account | [#19](https://github.com/KaustubhMukdam/devops-capstone-project/pull/19) | Done, issue closed | `delete-accounts.png` — pending focused capture |
| List and filter accounts | [#20](https://github.com/KaustubhMukdam/devops-capstone-project/pull/20) | Done, issue closed | `list-accounts.png` — pending focused capture |

The public [Sprint board](https://github.com/users/KaustubhMukdam/projects/3/views/6) shows the five Sprint 1 stories in Done and the Docker/Kubernetes stories in Icebox. The [setup.cfg](https://github.com/KaustubhMukdam/devops-capstone-project/blob/main/setup.cfg) URL is the AI-graded setup evidence. Because the stories were already completed before screenshots were requested, the user is capturing each completed card separately with its full title and Done status visible. These will be final-state captures, not five historical board states. The browser surface was unavailable to this session.

## Test and live API evidence

The [final Nose output](module-2-tests.txt) records **29 passing tests and 96% service coverage**. Flake8 reported zero findings. Each API call below was run against the local PostgreSQL-backed service, in the order specified by the handout. These text files contain the command, HTTP response, and JSON output where applicable.

| Function | AI-graded evidence | Result |
|---|---|---|
| Create | [rest-create-done.txt](rest-create-done.txt) | 201; account ID 1 and Location header |
| List | [rest-list-done.txt](rest-list-done.txt) | 200; array containing account 1 |
| Read | [rest-read-done.txt](rest-read-done.txt) | 200; account 1 |
| Update | [rest-update-done.txt](rest-update-done.txt) | 200; phone changed to 555-1111 |
| Delete | [rest-delete-done.txt](rest-delete-done.txt) | 204; empty body |

The demo request bodies are saved as [demo-create.json](demo-create.json) and [demo-update.json](demo-update.json), so the recorded `curl` commands are reproducible from the repository root. The sample account data is fictional.
