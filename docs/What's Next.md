## Priorities for the next iterations

- [ ] Update the project and documenttion to reflect the new changes in Tailwind 4
- [ ] Add a script to generate a seed file
- [ ] Add the section on how to use AI/CURSOR and the given rules and prompts library
- [ ] Add Drizzle ORM to move from a migration file based db to a schema based db

## Keep your project aligned with Flint

These steps are compltely optional, but recommended if you want to incorporate new changes from Flint updates into your derived project.

**Add the Flint repository as remote in your project**

```bash
git remote add flint https://github.com/mnlcpc/flint.git
```

**Create and move to a new branch to test the changes**

```bash
git checkout -b test-flint-update
```

**Fetch the latest changes from the Flint repository**

```bash
git fetch flint
```

**Merge the latest changes from the Flint repository into your project**

```bash
git merge flint/main
```

At this point you can resolve any merge conflicts, if any, and test the changes.
Once you are happy with the changes, you can merge the changes into your staging or main branch.
