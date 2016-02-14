# GITR

Run git commands in multiple git repositories recursively

## Example

Assuming this project structure:

    project/
        .git/
        sub-projects/
            sub-project-1/
                .git/
            sub-project-2/
                .git/
        dependencies/
            dependency-1/
                .git/
        ... and so on ...

then

    $ pwd
    project
    $ gitr status

will recurcively call `git status` on the `project` git repository and all other repositories that could be found under it: `sub-project-1`, `sub-project-2`, `dependency-1` and so on.
