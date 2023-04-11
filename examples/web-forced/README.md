## Remarks

* 1 (and only 1) `.csproject` under `src/`
* 1 (and only 1) `.csproject` under `tests/`

## Folder Structure

```
│   .gitignore
│   My.Site.sln
│   stylecop.json
|
│   .dockerignore
│   docker-compose.yml
│   Dockerfile
|   ...
│
├───.github/
│   └───workflows/
|       └ ...
|
├───azure/
│   ├───pipelines/
|   |   └ ...
│   └───policies/
|       └ ...
|
├───node_modules/
|   └ ...
|
├───scripts/
│   └ ...
|
├───src/
|
├───terraform
|       main.tf
|       output.tf
|       providers.tf
|       values.tf
|
└───tests/
```

## Analysis

### Pros

* `src/` & `tests/` are more familiar form developers that come from a Web App background
* Having 1 `src` forces focus on the project, incentivizing multi-repo (1-repo-per-project), in allignment with "12 Factors".

### Cons

* A folder like `terraform/` shows between `src/` & `tests/`
* Cannot cleanly add another `.csproject` (even for migrations).
* Cannot separate Testing by Unit|Integration|Acceptance, forcing to either
  * Run all of them.
  * Maintain Test PlayLists.
