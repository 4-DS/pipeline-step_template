# pipeline-step_template

Prerequisites

- Sinara is successfully deployed as described in [SinaraML Tutorial](https://github.com/4-DS/sinara-tutorials/wiki/Getting-started-with-SinaraML)

# Step repository naming conventions

We will recommend forming the git repo name as: <%pipeline_name>-<%step_name>

But this is not a mandatory requirement. And our library should work under any layouts with naming

The authoritative source of the pipeline and step names will now be exclusively in configs, and will not be tightly tied to the names of folders and git repositories


Make the following to create your Sinara step:

1. Create empty git repo with https://github.com/<%organization_name>/<%pipeline_name>-<%step_name>.git 
2. Clone the dsml component template repository
- cd work
- git clone --recurse-submodules https://github.com/4-DS/pipeline-step_template.git {my_step}
3. Change dsml component remote origin
- cd {my_step}
- git remote set-url origin https://github.com/<%organization_name>/<%pipeline_name>-<%step_name>.git
4. Squash dsml component template commits
- cd {my_step}
- git reset $(git commit-tree HEAD^{tree} -m "a new Sinara step")
5. Push dsml component template to new origin
- git push
6. See the [Getting Started](https://github.com/4-DS/sinara-tutorials/wiki/Getting-started) for details
